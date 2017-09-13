---
title: "동시성 런타임과 기타 동시성 모델 비교 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "동시성 런타임, 다른 모델과 비교"
ms.assetid: d8b9a1f4-f15f-43c3-a5b4-c0991edf9c86
caps.latest.revision: 18
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 18
---
# 동시성 런타임과 기타 동시성 모델 비교
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

이 문서에서는 동시성 런타임과 기타 기술의 기능 및 프로그래밍 모델 간 차이점에 대해 설명합니다. 동시성 런타임의 이점을 다른 프로그래밍 모델의 이점과 비교하는 방법을 이해하면 응용 프로그램 요구 사항에 가장 적합한 기술을 선택할 수 있습니다.  
  
 현재 Windows 스레드 풀, OpenMP 등의 다른 프로그래밍 모델을 사용하는 경우, 상황에 따라 동시성 런타임으로 마이그레이션하는 것이 적절할 수 있습니다. 예를 들어 [Migrating from OpenMP to the Concurrency Runtime](../../parallel/concrt/migrating-from-openmp-to-the-concurrency-runtime.md) 항목에서는 OpenMP에서 동시성 런타임으로 마이그레이션하는 것이 적절한 시기에 대해 설명합니다. 그러나 응용 프로그램 성능 및 현재 디버깅 지원에 만족하는 경우 마이그레이션이 필요하지 않습니다.  
  
 다른 동시성 모델을 사용하는 기존 응용 프로그램을 보완하기 위해 동시성 런타임의 기능 및 생산성 이점을 사용할 수 있습니다. 여러 작업 스케줄러가 같은 컴퓨팅 리소스에 대해 경쟁하는 경우 동시성 런타임에서 부하 분산을 보장할 수 없습니다. 그러나 작업이 겹치지 않을 경우 이 효과는 최소화됩니다.  
  
##  <a name="a-nametopa-sections"></a><a name="top"></a> 섹션  
  
-   [선점형 일정을 협조적 일정과 비교](#models)  
  
-   [동시성 런타임을 Windows API와 비교](#winapi)  
  
-   [동시성 런타임을 OpenMP와 비교](#openmp)  
  
##  <a name="a-namemodelsa-comparing-preemptive-scheduling-to-cooperative-scheduling"></a><a name="models"></a> 선점형 일정을 협조적 일정과 비교  
 선점형 일정 모델과 협조적 일정 모델은 여러 작업이 프로세서나 하드웨어 스레드 같은 컴퓨팅 리소스를 공유하도록 해주는 두 가지 일반적인 방법입니다.  
  
### <a name="preemptive-and-cooperative-scheduling"></a>선점형 일정 및 협조적 일정  
 *선점형 일정* 은 지정된 시간 동안 모든 작업에 번갈아가며 컴퓨팅 리소스에 대한 독점적 액세스를 제공하는 우선 순위 기반의 라운드 로빈 메커니즘입니다. 선점형 일정은 Windows와 같은 멀티태스킹 운영 체제에서 일반적입니다*. 협조적 일정*은 작업이 완료될 때까지 또는 작업이 액세스를 다른 리소스에 양보할 때까지 모든 작업에 컴퓨팅 리소스에 대한 독점적 액세스를 제공하는 메커니즘입니다. 동시성 런타임은 처리 리소스를 최대한 사용하기 위해 협조적 일정을 운영 체제의 선점형 스케줄러와 함께 사용합니다.  
  
### <a name="differences-between-preemptive-and-cooperative-schedulers"></a>선점형 스케줄러와 협조적 스케줄러의 차이점  
 선점형 스케줄러는 여러 스레드에 컴퓨팅 리소스에 대한 동일한 액세스를 제공하여 모든 스레드가 진행될 수 있도록 합니다. 컴퓨팅 리소스가 많은 컴퓨터에서는 공정한 액세스를 보장하는 것은 별로 문제가 되지 않으며, 오히려 리소스의 충분한 활용을 보장하는 것이 더 문제가 됩니다.  
  
 선점형 커널 모드 스케줄러에서는 응용 프로그램 코드가 운영 체제를 사용하여 일정을 결정해야 합니다. 반대로, 사용자 모드 협조적 스케줄러는 응용 프로그램 코드가 스스로 일정을 결정하도록 합니다. 협조적 일정의 경우 응용 프로그램이 많은 일정 결정을 내리기 때문에 커널 모드 동기화와 관련된 오버헤드가 상당히 줄어듭니다. 일반적으로 협조적 스케줄러는, 운영 체제 커널에 예약할 다른 작업이 없는 경우 운영 체제 커널에서 일정을 결정하도록 합니다. 또한 협조적 스케줄러는 커널에 전달되는 차단 작업이 있을 경우 운영 체제 스케줄러에서 일정을 결정하도록 하지만, 해당 작업은 사용자 모드 스케줄러에 전달되지 않습니다.  
  
### <a name="cooperative-scheduling-and-efficiency"></a>협조적 일정 및 효율성  
 선점형 스케줄러에 대해서는 동일한 우선 순위를 가진 모든 작업이 동등합니다. 일반적으로 선점형 스케줄러는 생성된 순서대로 스레드를 예약합니다. 또한 선점형 스케줄러는 스레드 우선 순위에 따라 라운드 로빈 방식으로 모든 스레드에 시간을 배분합니다. 이 메커니즘은 공정하지만(모든 스레드가 진행됨) 효율성 면에서는 다소 떨어집니다. 예를 들어 계산 집중적인 많은 알고리즘에는 공정성이 필요하지 않습니다. 대신 관련 작업을 최소한의 시간에 마치는 것이 중요합니다. 협조적 일정에서는 응용 프로그램이 좀 더 효율적으로 작업을 예약할 수 있습니다. 많은 스레드가 있는 응용 프로그램을 예로 들 수 있습니다. 동시에 실행되는 리소스를 공유하지 않는 스레드를 예약하면 동기화 오버헤드를 줄이는 한편 효율성을 높일 수 있습니다. 작업을 예약하는 또 다른 효율적인 방법은, 각 파이프라인 단계의 입력이 메모리 캐시에 이미 로드되도록 동일한 프로세서에서 작업의 파이프라인(각 작업이 이전 작업의 출력을 기반으로 작동)을 실행하는 것입니다.  
  
### <a name="using-preemptive-and-cooperative-scheduling-together"></a>선점형 일정과 협조적 일정을 함께 사용  
 협조적 일정이 모든 일정 문제를 해결하지는 못합니다. 예를 들어 다른 작업에 공정하게 양보하지 않는 작업은 사용 가능한 컴퓨팅 리소스를 모두 소비함으로써 다른 작업이 진행되는 것을 방해할 수 있습니다. 동시성 런타임은 협조적 일정의 효율성 이점을 사용하여 선점형 일정의 공정성 보장을 보완합니다. 기본적으로 동시성 런타임은 작업 가로채기 알고리즘을 사용하는 협조적 스케줄러를 제공하여 컴퓨팅 리소스 간에 작업을 효율적으로 배포합니다. 하지만 동시성 런타임 스케줄러는 또한 운영 체제의 선점형 스케줄러를 사용하여 응용 프로그램 간에 리소스를 공정하게 배포합니다. 스레드 실행을 세부적으로 제어하기 위해 응용 프로그램에서 사용자 지정 스케줄러 및 스케줄러 정책을 만들 수 있습니다.  
  
 [[맨 위로 이동](#top)]  
  
##  <a name="a-namewinapia-comparing-the-concurrency-runtime-to-the-windows-api"></a><a name="winapi"></a> 동시성 런타임을 Windows API와 비교  
 Windows API(이전의 Win32)라고도 하는 Microsoft Windows 응용 프로그래밍 인터페이스는 응용 프로그램에서 동시성을 가능하게 하는 프로그래밍 모델을 제공합니다. 동시성 런타임은 Windows API를 기반으로 구축되어 기본 운영 체제에서 사용할 수 없는 추가 프로그래밍 모델을 제공합니다.  
  
 동시성 런타임은 Windows API 스레드 모델을 기반으로 구축되어 병렬 작업을 수행합니다. 또한 Windows API 메모리 관리 및 스레드 로컬 저장소 메커니즘을 사용합니다. Windows 7 및 Windows Server 2008 R2에서 동시성 런타임은 사용자가 예약할 수 있는 스레드 및 64개가 넘는 하드웨어 스레드를 가지고 있는 컴퓨터에 대해 Windows API 지원을 사용합니다. 동시성 런타임은 협조적 작업 스케줄러 및 작업 가로채기 알고리즘을 제공하여 컴퓨팅 리소스의 사용을 최대화하고 여러 동시 스케줄러 인스턴스를 사용하도록 설정함으로써 Windows API 모델을 확장합니다.  
   
### <a name="programming-languages"></a>프로그래밍 언어  
 Windows API는 프로그래밍 모델을 노출하기 위해 C 프로그래밍 언어를 사용합니다. 동시성 런타임은 C++ 언어의 최신 기능을 활용하는 C++ 프로그래밍 인터페이스를 제공합니다. 예를 들어, 람다 함수는 병렬 작업 함수를 정의하기 위한 간결하고 형식이 안전한 메커니즘을 제공합니다. 동시성 런타임을 사용하는 최신 C++ 기능에 대한 자세한 내용은 [개요](../../parallel/concrt/asynchronous-message-blocks.md)를 참조하세요.  
  
### <a name="threads-and-thread-pools"></a>스레드 및 스레드 풀  
 Windows API의 중심적인 동시성 메커니즘은 스레드입니다. 일반적으로 [CreateThread](http://msdn.microsoft.com/library/windows/desktop/ms682453) 함수를 사용하여 스레드를 만듭니다. 스레드는 비교적 쉽게 만들고 사용할 수 있지만 운영 체제는 스레드 관리에 상당한 양의 시간과 기타 리소스를 할당합니다. 또한 각 스레드는 우선 순위 수준이 같은 다른 스레드와 동일한 실행 시간을 이용하도록 보장되지만, 관련된 오버헤드는 충분히 큰 작업을 만들도록 요구합니다. 더 작거나 더 세분화된 작업의 경우, 동시성과 관련된 오버헤드가 병렬 작업 실행의 이점보다 클 수 있습니다.  
  
 스레드 풀은 스레드 관리의 비용을 줄이기 위한 한 가지 방법입니다. 사용자 지정 스레드 풀 및 Windows API에서 제공하는 스레드 풀 구현, 이 두 가지를 통해 작은 작업 항목들이 효율적으로 동시에 실행됩니다. Windows 스레드 풀은 FIFO(선입선출) 큐에서 작업 항목을 유지 관리합니다. 각 작업 항목은 풀에 추가된 순서로 시작됩니다.  
  
 동시성 런타임은 작업 가로채기 알고리즘을 구현하여 FIFO 예약 메커니즘을 확장합니다. 이 알고리즘은 아직 시작되지 않은 항목을 작업 항목이 모두 소모된 스레드로 이동합니다. 작업 가로채기 알고리즘을 통해 부하가 분산될 수는 있지만 작업 항목을 다시 정렬해야 하는 상황이 발생할 수도 있습니다. 다시 정렬하는 이 프로세스에서는 작업 항목이 원래 제출된 것과 다른 순서로 시작될 수 있습니다. 이는 데이터가 이전 작업들보다는 새 작업들 간에 공유될 수 있는 더 나은 기회가 있는 재귀 알고리즘에 유용합니다. 새 항목을 먼저 실행한다는 것은 캐시 누락이 줄어들고 이에 따라 페이지 폴트도 줄어들 수 있음을 의미합니다.  
  
 운영 체제의 관점에서 작업 가로채기는 공정하지 않습니다. 그러나 응용 프로그램이 병렬로 실행되는 알고리즘이나 작업을 구현할 때 하위 작업들 간의 공정성이 항상 중요한 것은 아닙니다. 중요한 것은 전체 작업이 얼마나 빨리 완료되는가 하는 것입니다. 다른 알고리즘에도 FIFO는 적절한 일정 전략입니다.  
  
### <a name="behavior-on-various-operating-systems"></a>다양한 운영 체제에서 작동  
 Windows XP 및 Windows Vista에서 동시성 런타임을 사용하는 응용 프로그램은, Windows Vista에서에서 힙 성능이 향상되는 것을 제외하면 비슷하게 작동합니다.  
  
 Windows 7 및 Windows Server 2008 R2에서는 운영 체제가 동시성 및 확장성을 더 잘 지원합니다. 예를 들어, 이러한 운영 체제는 64개가 넘는 하드웨어 스레드가 있는 컴퓨터를 지원합니다. 이러한 새 기능을 활용하려면 Windows API를 사용하는 기존 응용 프로그램을 수정해야 합니다. 그러나 동시성 런타임을 사용하는 응용 프로그램은 자동으로 이러한 기능을 사용하므로 수정할 필요가 없습니다.  
  
 [base.user-mode_scheduling](http://msdn.microsoft.com/library/windows/desktop/dd627187)  
  
 [[맨 위로 이동](#top)]  
  
##  <a name="a-nameopenmpa-comparing-the-concurrency-runtime-to-openmp"></a><a name="openmp"></a> 동시성 런타임을 OpenMP와 비교  
 동시성 런타임은 다양한 프로그래밍 모델을 사용합니다. 이러한 모델은 중복되거나 다른 라이브러리의 모델을 보완할 수 있습니다. 이 섹션에서는 동시성 런타임을 [OpenMP](../../parallel/concrt/comparing-the-concurrency-runtime-to-other-concurrency-models.md#openmp_in_visual_c_add_add)와 비교합니다.  
  
 OpenMP 프로그래밍 모델은 공개 표준에 의해 정의되며, Fortran 및 C/C++ 프로그래밍 언어에 대한 잘 정의된 바인딩을 가지고 있습니다. OpenMP 버전 2.0 및 2.5는 반복적인 병렬 알고리즘에 적합합니다. 즉, 일련의 데이터에 대한 병렬 반복을 수행합니다. OpenMP는 병렬 처리 수준이 미리 결정되어 있고 시스템에서 사용 가능한 리소스와 일치할 때 가장 효율적입니다. OpenMP 모델은 매우 큰 규모의 계산 문제가 단일 컴퓨터의 처리 리소스 간에 배포되어 있는 고성능 컴퓨팅 환경에 특히 적합합니다. 이 시나리오에서는 하드웨어 환경이 알려져 있으며, 개발자는 알고리즘이 실행될 때 컴퓨팅 리소스에 단독으로 액세스할 수 있을 것이라고 합리적으로 예상할 수 있습니다.  
  
 그러나 제약이 덜한 다른 환경에서는 OpenMP의 적합성이 떨어질 수 있습니다. 예를 들어 재귀적 문제(예: 빠른 정렬 알고리즘 또는 데이터 트리 검색)는 OpenMP를 사용하여 구현하기가 더 어렵습니다. 동시성 런타임은 PPL [(병렬 패턴 라이브러리)](../../parallel/concrt/parallel-patterns-library-ppl.md) 및 [비동기 에이전트 라이브러리](../../parallel/concrt/asynchronous-agents-library.md)를 제공하여 OpenMP의 기능을 보완합니다. OpenMP와는 달리 동시성 런타임은 사용 가능한 리소스에 맞게 수정되고 작업 변화에 따라 병렬 처리 수준을 조정하는 동적 스케줄러를 제공합니다.  
  
 동시성 런타임의 기능 중 다수는 확장 가능합니다. 기존 기능을 결합하여 새 기능을 구성할 수도 있습니다. OpenMP는 컴파일러 지시문에 의존하므로 쉽게 확장할 수 없습니다.  
  
 동시성 런타임을 OpenMP와 비교하는 방법 및 동시성 런타임을 사용하도록 기존 OpenMP 코드를 마이그레이션하는 방법에 대한 자세한 내용은 [Migrating from OpenMP to the Concurrency Runtime](../../parallel/concrt/migrating-from-openmp-to-the-concurrency-runtime.md)을 참조하세요.  
  
 [[맨 위로 이동](#top)]  
  
## <a name="see-also"></a>참고 항목  
 [동시성 런타임](../../parallel/concrt/concurrency-runtime.md)     
 [개요](../../parallel/concrt/asynchronous-message-blocks.md)   
 [PPL(병렬 패턴 라이브러리)](../../parallel/concrt/parallel-patterns-library-ppl.md)   
 [비동기 에이전트 라이브러리](../../parallel/concrt/asynchronous-agents-library.md)   
 [OpenMP](../../parallel/concrt/comparing-the-concurrency-runtime-to-other-concurrency-models.md#openmp_in_visual_c_add_add)