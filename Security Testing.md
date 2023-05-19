# Security Testing
## Authentication & Authorization
Authentication(인증)은 사용자 이름과 암호를 요구하여 사용자 또는 시스템의 ID를 확인하는 프로세스이다.     
사용자 ID가 Authentication(인증)되면 Authorization(권한 부여)는 사용자가 시스템 내에서 수행할 수 있는 작업을 결정하는 프로세스이다.     
Authorization(권한 부여)는 특정 사용자에게 할당된 역할 및 권한을 통해 관리한다.
 
## 장단점
### 장점
* 중요한 정보 또는 작업에 대한 액세스를 제어하여 보안을 강화
* 관리자가 역할 및 권한에 따라 사용자 액세스 수준을 관리
* 개별 사용자의 액션을 추적하여 책임 및 감사 기능을 개선
### 단점
* 사용자 역할 및 권한을 적절하게 관리하려면 추가 설정과 구성이 필요
* 다양한 사용자 역할과 권한을 가진 대규모 시스템에서 구현 복잡

## Vulnerability Scanning
Vulnerability Scanning(취약성 검사)은 자동화된 도구를 사용하여 소프트웨어 시스템 또는 네트워크의 잠재적인 보안 취약성을 식별하는 프로세스이다.    
Vulnerability Scanning(취약성 검사)을 정기적으로 수행하여 발견된 새로운 취약성을 식별하거나 이전에 식별된 취약성이 해결되었는지 확인할 수 있다.

## 장단점
### 장점
* 잠재적인 보안 취약성을 공격하기 전에 식별 가능
* 식별된 취약성을 완화하기 위해 사전 조치 가능
* 지속적인 보안을 보장하기 위해 정기적으로 자동화 수행 가능
### 단점
* 실제 취약성이 아닌 문제를 식별하는 잘못된 긍정을 생성 가능
* 새로운 취약성이 지속적으로 발견되기 때문에 모든 잠재적 취약성을 식별 불가능
* 식별된 취약성을 분석하고 해결하는 데 많은 시간이 소요

## OWASP (Open Web Application Security Project) 10 
OWASP Top 10은 OWASP(Open Web Application Security Project)에서 개발한 가장 중요한 웹 애플리케이션 보안 위험 목록이다.    
상위 10가지 위험 요소:
1. Injection (주사)
2. Broken authentication and session management (고장난 인증과 세션 관리)
3. Cross-site scripting (사이트 간 스크립팅(XSS))
4. Broken access control (고장난 접근통제)
5. Security misconfiguration (보안 구성 오류)
6. Insecure cryptographic storage (안전하지 않은 암호화 저장소)
7. Insufficient logging and monitoring (불충분한 로깅과 모니터링)
8. Insecure communication (불안정한 의사소통)
9. Using components with known vulnerabilities (알려진 취약성이 있는 구성 요소 사용)
10. Insufficient protection of sensitive data (민감한 데이터에 대한 불충분한 보호)

## 장단점
### 장점
* 가장 중요한 웹 응용프로그램 보안 위험에 대한 포괄적이고 업데이트된 목록 제공
* 가장 중요한 보안 문제에 우선 순위를 지정하고 집중할 수 있도록 지원
* 보안 응용프로그램을 설계, 개발 및 테스트할 수 있도록 지원

### 단점
* 상위 10개의 리스크만 다루며, 조직과 서비스에 특정한 다른 리스크가 존재 가능
* 목록은 시간이 지남에 따라 변경될 수 있으며, 조직은 변경사항과 업데이트를 지속적으로 확인해야 함

## Attack Vectors
Attack Vectors는 시스템의 취약성 또는 약점을 이용하여 공격을 수행할 수 있는 방법이다.    
Attack Vectors는 네트워크 기반 공격, 애플리케이션 수준 공격, 소셜 엔지니어링 공격, 물리적 공격과 같은 다양한 범주로 분류할 수 있다.

## 장단점
### 장점
* 조직이 시스템의 취약점을 악용할 수 있는 다양한 방법을 식별하고 이해할 수 있도록 지원한다.
* 공격을 방지하기 위한 효과적인 보안 조치를 설계하고 구현하는 데 도움이 된다.

### 단점
* 지속적으로 진화하고 있으며 최신 공격 기술을 따라잡기 어려울 수 있다.
* 일부는 탐지와 방지하기 어려울 수 있다.

## Secrets Management
Secrets Management는 암호, API 키와 기타 자격 증명과 같은 중요한 정보를 안전하게 저장하고 관리하는 프로세스이다.    
Secrets Management는 키 관리 시스템과 비밀 관리 서비스 같은 다양한 도구를 사용하여 수행할 수 있다.

## 장단점
### 장점
* 중요한 정보를 안전하게 저장하고 관리 가능
* 무단 액세스와 데이터 침해 방지

### 단점
* 구현의 복잡성과 어려움
* 추가 리소스와 투자 필요


### 참고
https://www.okta.com/kr/identity-101/authentication-vs-authorization/    
https://www.beyondtrust.com/resources/glossary/vulnerability-scanning      



