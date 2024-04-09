## 브랜치 관리의 필요성
- 서로의 작업에 영향을 주지 않기 위해 브랜치의 분리 필요함 <br/>
- 각 브랜치가 어떤 작업을 위해 존재하는지 구분 필요함 <br/>
- main 브랜치의 안전한 관리 필요함 <br/>

## 브랜치 보호 규칙
- 승인 없이 pull request 병합할 수 없도록 제한 가능 <br/>
- 특정 branch에 push 가능자를 제한 가능

## 브랜치 전략
### git flow
2010년에 Vincent Driessen이 고안한 방법
#### main branches
제거 x
##### main(master) 
- 프로젝트 생성 시 기본으로 생성되는 브랜치 <br/>
- 병합될 때마다 새로운 버전
##### develop
- feature의 기본

#### supporting branches
##### feature
- develop branch에서 분기하여 작업 <br/>
- 대부분 이름 가능
##### release
- 배포 준비를 위한 branch <br/>
- 버그 수정, QA 작업 후 main에 병합
##### hotfix
- 배포 환경에서 즉각적인 수정이 필요한 경우 <br/>
- main, develop 모두에 병합

### github flow
요즘은 이거 씀
#### main
- 항상 배포 가능 상태로 유지 <br/>
- main으로 병합 전에 충분한 test 필요

#### feature
- branch 목적을 이름에 잘 담아야함 <br/>
- 코드 리뷰 매우 중요

## 개발자로서의 태도
### convention 지키기
- 의도 파악이 쉬움 <br/>
- 보기 좋음
### 구글링 잘하기
핑프 멈춰
### 코드 주인의식 가지기
public repository는 누구나 봄
### 좋은 질문하기
좋은 질문하기 위해 노력하기