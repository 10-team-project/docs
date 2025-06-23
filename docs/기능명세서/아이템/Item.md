# 기능 명세서: [아이템 기본]

## 📌 기능 개요
- **기능 설명**: 여러가지 유형의 아이템을 만들 수 있는 기초
- **담당자**: [신희관]
- **개발 일자**: [2025-06-20]
- **관련 이슈/티켓**:  N/A

---

## 🧩 클래스 구조 및 역할

### 1. 클래스명: Item
- **역할**: ItemData 클래스를 가지고 있고 다른 Item 클래스들의 부모 역할
- **주요 메서드**: 없음	
- **상속/인터페이스**:
  - 상속: 없음
  - 구현 인터페이스: 구현 예정

### 2. 관련 클래스/컴포넌트
- [ItemData](https://10-team-project.github.io/docs/%EA%B8%B0%EB%8A%A5%EB%AA%85%EC%84%B8%EC%84%9C/%EC%95%84%EC%9D%B4%ED%85%9C/ItemData/) Item의 정보를 가지고 있음
- [Inventory](https://10-team-project.github.io/docs/%EA%B8%B0%EB%8A%A5%EB%AA%85%EC%84%B8%EC%84%9C/%EC%95%84%EC%9D%B4%ED%85%9C/Invetory/)에서 사용됨

---

## 클래스 다이어그램
```mermaid
classDiagram
	class Item {
	<<abstract>>
		+Data: ItemData
		-data: ItemData
		+Item(ItemData data) Item
	}

	class ItemData {
		<<abstract>>
		+Name: string
		+Image: Sprite
		+Prefab: GameObject
		
		-itemName: string
		-image: Sprite
		-prefab: GameObject	

		#IsNameEmpty() bool
		#IsImageNone() bool
[]()		#IsPrefabNone() bool
	}

	Item "*" o-- "1" ItemData	: has
```