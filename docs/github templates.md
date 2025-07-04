**깃허브 탬플릿 예시**
# 이슈 탬플릿
## 1번
```yaml
	name: 기능 추가 요청
	description: 새로운 기능이나 시스템 추가를 위한 이슈 템플릿입니다.
	title: "[Feature] 기능 이름 요약"
	labels: ["feature", "pending"]
	assignees:
		- 작성자GitHubID
	
	body:
		- type: input
			id: summary
			attributes:
				label: 📝 기능 요약
				description: 구현할 기능을 간단하게 설명해주세요.
				placeholder: ex) 플레이어 점프 기능 추가
			validations:
				required: true
	
		- type: textarea
			id: detail
			attributes:
				label: 📌 상세 설명
				description: 기능의 동작 방식, 주요 흐름, 기대 효과 등을 자세히 작성해주세요.
				placeholder: |
					- 스페이스바 입력 시 캐릭터 점프
					- 장애물 회피를 위한 기능
			validations:
				required: true
	
		- type: textarea
			id: classplan
			attributes:
				label: 🧩 예상 클래스 및 메서드
				description: 예상되는 클래스 이름, 책임, 주요 메서드를 간단히 정리해주세요.
				placeholder: |
					- JumpController: 입력 감지 및 점프 처리
					- PhysicsHandler: 중력 적용
			validations:
				required: false
	
		- type: textarea
			id: note
			attributes:
				label: 📝 참고 사항
				description: 관련 문서, 디자인 참고 자료, 또는 이슈 간 링크가 있다면 적어주세요.
				placeholder: ex) #42 이동 시스템과 연계 필요
	
		- type: checkboxes
			id: checklist
			attributes:
				label: ✅ 체크리스트
				description: 아래 항목을 확인해주세요.
				options:
					- label: 해당 기능은 중복되지 않습니다.
						required: true
					- label: 다른 팀원과 협업 범위를 확인했습니다.
					- label: 명세서 작성을 염두에 두고 설계 중입니다.
```

---
## 2번 
```yaml
name: 기능 요청
description: 새로운 기능 개발을 위한 이슈
title: "[Feature] 기능 이름"
labels: ["feature"]
body:
  - type: input
    id: summary
    attributes:
      label: 기능 요약
      placeholder: ex) 플레이어 점프 기능
    validations:
      required: true

  - type: textarea
    id: details
    attributes:
      label: 기능 설명
      placeholder: 어떤 동작인지 간단히 설명해주세요
    validations:
      required: true

  - type: textarea
    id: design
    attributes:
      label: 예상 클래스 / 메서드
      placeholder: 클래스명, 주요 책임 등 (선택)
    validations:
      required: false

  - type: checkboxes
    id: checklist
    attributes:
      label: 확인 사항
      options:
        - label: 중복된 기능이 아닙니다
        - lab

```

---
# 버그 리포트 탬플릿
## 1번
```yaml
name: 버그 리포트
description: 발생한 문제를 보고합니다.
title: "[Bug] 문제 요약"
labels: ["bug"]
body:
  - type: input
    id: summary
    attributes:
      label: 버그 요약
      placeholder: ex) 게임 실행 시 캐릭터가 움직이지 않음
    validations:
      required: true

  - type: textarea
    id: steps
    attributes:
      label: 재현 방법
      placeholder: |
        1. 게임 시작
        2. W 키 입력
        3. 캐릭터가 정지 상태 유지
    validations:
      required: true

  - type: textarea
    id: expected
    attributes:
      label: 기대 동작
      placeholder: ex) W 키를 누르면 캐릭터가 앞으로 이동해야 함
    validations:
      required: false

  - type: textarea
    id: env
    attributes:
      label: 실행 환경
      placeholder: |
        - OS: Windows 10
        - Unity 버전: 2022.3.1f
        - 플랫폼: PC
    validations:
      required: false

  - type: checkboxes
    id: checklist
    attributes:
      label: 확인 사항
      options:
        - label: 최신 버전에서 테스트했습니다
        - label: 중복된 이슈가 없는지 확인했습니다

```

---
## 2번
```yaml
name: 버그 리포트
description: 문제가 발생했을 때 작성해주세요.
title: "[Bug] 문제 요약"
labels: ["bug"]
body:
  - type: input
    id: summary
    attributes:
      label: 문제 요약
      placeholder: ex) 캐릭터가 점프하지 않음
    validations:
      required: true

  - type: textarea
    id: steps
    attributes:
      label: 재현 방법
      placeholder: 어떤 상황에서 버그가 발생했는지 간단히 써주세요
    validations:
```

---
# PR 탬플릿
## 1번
## ✨ PR 내용 요약
- 어떤 기능/수정을 했는지 간단히 설명해주세요.

## 📌 관련 이슈
- Close #이슈번호 (선택)

## 🧪 확인 사항
- [ ] 기능이 정상 작동합니다
- [ ] 코드 리뷰를 위한 주석/테스트가 적절히 포함되어 있습니다
- [ ] 기존 기능에 영향이 없습니다

## 💬 기타 참고 사항
- 필요 시 작성해주세요 (예: 테스트 방법, 디자인 참고 링크 등)


---
## 2번
## 📌 개요
- 어떤 변경이 있었는지 요약해주세요.
- 관련 이슈가 있다면 아래에 링크를 남겨주세요.

예: Close #42

## 🔍 변경 사항
- [ ] 기능 추가
- [ ] 버그 수정
- [ ] 리팩토링
- [ ] UI 변경
- [ ] 문서/주석 수정

## 🧪 테스트 내역
- 어떤 테스트를 했는지, 어떻게 확인했는지 간단히 적어주세요.

## ✅ 작성자 체크리스트
- [ ] 로컬에서 정상 작동 확인
- [ ] 관련 테스트 또는 케이스 작성
- [ ] 기존 기능에 영향 없는지 확인
- [ ] 충돌 없는 최신 main/dev 브랜치 기준으로 작성됨

## 
👀 리뷰어 참고사항
- [ ] 코드 구조/가독성 괜찮은지
- [ ] 클래스/메서드 역할이 명확한지
- [ ] 중복되거나 불필요한 로직 없는지
- [ ] 네이밍 규칙 및 컨벤션 맞는지

---

## 3번 게임용

## 🧩 개요
- 이 PR에서 어떤 기능이 추가/수정되었는지 간략히 설명해주세요.
- 관련 이슈: Close #

## ✅ 기능 체크리스트

- [ ] 기능이 의도한 대로 동작함
- [ ] 에디터 및 실행 중 오류 없음
- [ ] 관련 UI/애니메이션 정상 출력
- [ ] 기존 기능에 영향 없음
- [ ] 주요 기능에 대한 로그 또는 디버깅 정보 제거함

## 🔍 코드 구조 체크리스트

- [ ] 클래스 책임이 명확함 (단일 책임 원칙 등)
- [ ] 네이밍이 직관적이고 일관성 있음
- [ ] 매직 넘버 제거 및 상수화 처리
- [ ] 중복 코드 없음

## 🧪 테스트 체크리스트

- [ ] 로컬 테스트 완료
- [ ] 충돌 및 경계 상황 테스트 완료
- [ ] (선택) 단위 테스트/에디터 테스트 통과

## 📝 기타 참고사항
- 필요한 경우, 리뷰어가 참고할 영상/GIF, 스크린샷, 에디터 세팅 등을 여기에 첨부해주세요.

---
## 4번 유니티용
## 🧩 개요
- 이번 PR에서 변경된 핵심 내용을 간단히 적어주세요.
- 관련 이슈: Close #

## 📁 변경 사항 체크리스트

- [ ] C# 스크립트 추가/수정
- [ ] 프리팹 변경
- [ ] 씬(.unity) 파일 변경
- [ ] 애니메이션/사운드 리소스 변경
- [ ] ScriptableObject 변경
- [ ] 기타 리소스 또는 설정 변경

## ✅ 확인 사항

- [ ] Unity 에디터에서 정상 동작 확인
- [ ] 관련 기능 플레이 테스트 완료
- [ ] 에러/경고 없음
- [ ] 변경된 파일이 Git LFS 대상인지 확인 (필요시)
- [ ] 충돌 방지를 위해 최신 develop/main 브랜치에서 작업

## 🧪 테스트 내역

- [ ] 새 기능 직접 실행 확인
- [ ] 씬 변경 시, 기존 오브젝트와 충돌 없음
- [ ] 멀티플레이/네트워크 관련 기능 확인 (해당 시)
- [ ] (선택) 커스텀 유닛/에디터 테스트 포함

## 📝 기타

- [ ] 변경된 프리팹/씬이 **Unity 외부에서**

---

**폴더 구성**   
 .github/   
├── ISSUE_TEMPLATE/   
│   ├── feature-request.yaml      ← 기능 요청용 템플릿   
│   ├── bug-report.yaml           ← 버그 리포트용 템플릿   
│   └── config.yml                ← 템플릿 선택 화면 설정 파일   
├── pull_request_template.md      ← PR 템플릿   
