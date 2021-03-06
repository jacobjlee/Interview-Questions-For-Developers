# DevOps

### DevOps란?

**DevOps**란 **애플리케이션과 서비스를 빠른 속도로 제공할 수 있는 있도록 조직의 역량을 향상시키는 문화 철학, 방식 및 도구의 조합**이다. 기존의 소프트웨어 개발 및 인프라 관리 프로세스를 사용하는 조직보다 **제품을 더 빠르게 혁신하고 개선**할 수 있다. 이러한 빠른 속도를 통해 조직은 고객을 더 잘 지원하고 시장에서 좀 더 효과적으로 경쟁할 수 있다.

### DevOps에는 어떤 방식이 있는가?

DevOps의 모범 사례는 다음과 같다.

- 지속적 통합 (CI)
- 지속적 전달 (CD)
- 마이크로 서비스 (MSA)
- 코드형 인프라 (Infrastructure as Code)
- 모니터링 및 로깅
- 커뮤니케이션 및 협업

### CI란 무엇인가?

CI는 **Continuous Integration**의 줄임말로, **지속적인 통합**을 의미한다.
CI를 성공적으로 구현할 경우, 애플리케이션에 대한 새로운 코드 변경 사항이 정기적으로 빌드 및 테스트되어 공유 repository에 통합되므로 여러 명의 개발자가 동시에 애플리케이션 개발과 관련된 코드 작업을 할 경우 서로 충돌할 수 있는 문제를 해결할 수 있다.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/05ed288e-950e-439a-93be-57290db0e584/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210217%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210217T110435Z&X-Amz-Expires=86400&X-Amz-Signature=c5d896703ae3f9092cd39bf5ef274eccf2b8a00cf40124e9f5218da6ee0d4088&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

### CD란 무엇인가?

CD는 **지속적인 서비스 제공** (**Continuous Delivery)** 또는 **지속적인 배포(Continuous Deployment)** 를 의미하며, 두 용어는 상호 교환적으로 사용된다.

- **지속적인 제공**이란 개발자들이 애플리케이션에 적용한 변경 사항이 버그 테스트를 거쳐 repository에 자동으로 업로드되는 것을 뜻하며, 운영팀은 이 repository에서 애플리케이션을 실시간 프로덕션 환경으로 배포할 수 있다. 이는 개발팀과 비즈니스팀 간의 가시성과 커뮤니케이션 부족 문제를 해결해 준다. 또한 지속적인 제공은 최소한의 노력으로 새로운 코드를 배포하는 것을 목표로 한다.
- **지속적인 배포**란 개발자의 변경 사항을 repository에서 고객이 사용 가능한 프로덕션 환경까지 자동으로 release하는 것을 의미한다. 이는 애플리케이션 제공 속도를 저해하는 수동 프로세스로 인한 운영팀의 과부하 문제를 해결한다.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5e9c846d-7276-440c-b0fb-25fafafeb44e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210217%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210217T110506Z&X-Amz-Expires=86400&X-Amz-Signature=9b912210aacf9a3fc0f66d4144a38b11297976d23deb5c5add9f4f6c8bfa6dc4&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

### Jenkins vs. Travis CI vs. Circle CI

- **Jenkins**

    Jenkins는 **자바 기반**의 프로그램이다. 젠킨스는 플러그인 아키텍처를 통해 확장이 가능해서 거의 불가능 한 부분이 없을 정도로 많은 가능성을 제공한다. Jenkins는 dedicated server를 요구하기 때문에 추가적인 금액이 발생할 수 있고, configuration / customization 하는데 시간이 필요한 것이 단점이다.
    젠킨스는 플러그인을 통해 많은 커스터마이징이 가능하므로 **큰 프로젝트에 많이 사용**된다. 즉, 빠르게 CI 시스템을 사용해야 한다면 젠킨스는 좋은 선택이 아닐 수 있다.

- **Travis CI**

    Travis CI는 **클라우드 기반**의 서버이며, YAML file로 구성하고, 테스트를 실행하도록 docker를 지원한다.
    CI 시스템중에 가장 많은 언어를 지원한다. Travis CI는 빠르고, YAML config를 사용해 가볍고, 무료이지만 Circle CI와 비교했을 때, 기업 플랜이 더 비싸고 커스터마이징이 제한되어 있다.
    Travis CI는 여러 환경에서 테스트되야 하는 **오픈 소스 프로젝트**에 적합하다.

- **Circle CI**

    Circle CI 역시 **클라우드 기반**의 시스템이며 Travis CI와 매우 흡사하다. 즉, Circle CI는 YAML config로 가볍고, 빠르게 시작할 수 있다. Circle CI를 사용하면 dedicated sever(단독으로 제공된 서버 위에서 하나의 서비스를 제공하는 서비스)가 필요 없으며, 관리할 필요가 없어진다 (Travis CI 동일). 
    Circle CI는 최대한 빨리 통합해야하는 목적을 가진 **작은 프로젝트**에 적합하다. 

- 그 외, Gitlab CI, TeamCity같은 툴도 있다.

### Microservices Architecture란?

마이크로서비스는 **애플리케이션 구축을 위한 아키텍처 기반의 접근 방식**이다. 
마이크로서비스를 전통적인 monolithic 접근 방식과 구별 짓는 기준은, **애플리케이션을 핵심 기능으로 세분화하는 방식을 사용하는가**이다. 마이크로서비스에서는 **각 기능을 서비스**라고 부르고, **독립적으로 구축하고 배포**할 수 있다. 이렇게 함으로 개별 서비스가 다른 서비스에 부정적 영향을 주지 않으면서 작동(또는 장애가 발생)할 수 있다.

쉽게 비유하면, 어떤 쇼핑몰에 접속했을 때 보이는 검색창, 추천 내역, 장바구니, 이 모든 것이 하나의 서비스이다.
즉, 마이크로서비스란 **애플리케이션의 핵심 기능이면서 다른 서비스들과 독립적으로 작동**한다.
애플리케이션 핵심 기능을 유연하게 결합할 뿐 아니라, **불가피한 장애, 향후 확장 여부 및 새로운 기능 통합에 대비할 수 있도록 서비스 간 커뮤니케이션 및 개발팀의 구조를 조정**하는 practice이다.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/e99a45dc-6d8e-4339-b6d8-ad00d4717555/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210217%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210217T110509Z&X-Amz-Expires=86400&X-Amz-Signature=595b3ac56f0a7df580c1dc35f1826e105ebcb9a64735e332163a8c866304f50e&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

### 코드형 인프라란 무엇인가?

'**프로그래밍형 인프라**'라고도 불리는 **코드형 인프라 (Infrastructure as Code)** 는 인프라 구성을 마치 소프트웨어를 프로그래밍하는 것처럼 처리하는 방식을 가리킨다. 

### 코드형 인프라는 어떤 장점을 가지고 있는가?

- 빠른 속도와 편리함
- 수동 구성이 아닌 자동화로 일관성 있는 구성
- 실제 인프라에 적용하기 전 테스트 실행으로 위험 최소화
- 구성하고 싶은 인프라를 코드를 제출 - 업무효율 극대화
- 반복적인 작업을 자동화하고 인프라 구성 프로세스를 최적화 함으로 생산성 증가
