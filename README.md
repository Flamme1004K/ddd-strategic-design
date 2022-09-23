# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전

### 상품

| 한글명      | 영문명                   | 설명                                                                                     |
|----------|-----------------------|----------------------------------------------------------------------------------------|
| 상품       | product               | 키친포스에 등록될 상품을 의미한다. 상품 이름과 상품 가격을 반드시 입력해야 하고 상품 이름이 빈값이나 상품 가격은 0보다 작을 수 없다.          |
| 상품 이름    | product name          | 키친포스가 관리하는 상품의 이름                                                                      |
| 상품 가격    | product price         | 키친포스가 관리하는 상품의 가격                                                                      |
| 비속어      | profanity             | 욕설, 음란 표현 등, 부적절한 단어                                                                   |

### 메뉴 그룹

| 한글명      | 영문명               | 설명                                                            |
|----------|-------------------|---------------------------------------------------------------|
| 메뉴 그룹    | menu group        | 메뉴가 속하는 그룹을 의미한다.(추천 메뉴, 세트 메뉴 등),<br/>메뉴 그룹 이름은 반드시 입력해야 한다. |
| 메뉴 그룹 이름 | menu group name   | 메뉴 그룹의 이름                                                     |

### 메뉴

| 한글명     | 영문명           | 설명                                                            |
|---------|---------------|---------------------------------------------------------------|
| 메뉴      | menu          | 손님에게 판매할 하나 이상의 상품들의 묶음,<br/>이름, 가격, 메뉴 그룹, 구성상품목록으로 구성되어 있다. |
| 메뉴 이름   | menu name     | 메뉴의 이름, 메뉴 이름은 반드시 입력되어야 한다.                                  |
| 메뉴 가격   | menu price    | 메뉴의 가격, 메뉴 가격은 반드시 입력되고 0원 이상이어야 한다.                          |
| 메뉴 노출   | exposure menu | 손님에게 판매하려는 메뉴를 노출                                             |
| 메뉴 숨김   | hide menu     | 손님에게 메뉴를 숨김                                                   |
| 메뉴 속 상품 | menu product  | 메뉴에 속한 상품들                                                    |

### 주문 테이블

| 한글명          | 영문명                                 | 설명                                               |
|--------------|-------------------------------------|--------------------------------------------------|
| 주문 테이블       | order table                         | 매장 주문시 사용되는 매장 내 테이블                             |
| 주문 테이블 이름    | order table name                    | 주문 테이블의 이름, 이름은 반드시 입력 된다.                       |
| 손님           | guest                               | 매장 내 테이블을 이용하는 손님                                |
| 테이블 내 손님 수   | order table number of guests        | 주문 테이블을 이용하는 손님의 수                               |
| 주문 테이블 빈 테이블 | order table occupied                | 매장 내 주문 테이블의 사용 여부,<br/>손님이 착석하고 있으면 이용할 수 없다.   |
| 테이블 손님 착석    | order table guests sit              | 매장 내 주문 테이블에 손님이 착석한다.                           |
| 테이블 정리       | order table clear                   | 매장 내 주문 테이블를 이용한 손님들이 나간 후 테이블을 정리한다.            |

### 주문

| 한글명      | 영문명                     | 설명                                                                                                        |
|----------|-------------------------|-----------------------------------------------------------------------------------------------------------|
| 주문       | order                   | 손님이 노출된 메뉴를 하나 이상 구매                                                                                      |
| 주문 유형    | order type              | 주문 유형, 배달, 포장, 매장 존재                                                                                      |
| 주문 상태    | order status            | 주문 상태, 주문 대기, 주문 접수, 주문 서빙, 주문 배달중, 주문 배달 완료, 주문 완료 존재                                                    |
| 주문 메뉴    | order menu              | 손님이 주문한 주문의 최소 단위                                                                                         |
| 주문 금액    | order price             | 손님이 주문한 금액                                                                                                |
| 배달 주소    | delivery address        | 배달 손님의 주소                                                                                                 |
| 주문 접수 대기 | order waiting           | 주문은 되었으나 매장 직원이 확인하지 않은 상태                                                                                |
| 주문 접수    | order accepted          | 매장 직원이 주문을 확인하고 메뉴를 준비하는 상태                                                                               |
| 주문 서빙    | order served            | 메뉴를 완성 후 손님에게 서빙하는 상태                                                                                     |
| 배달 시작    | order delivery start    | 배달 기사분께서 매장에서 메뉴를 전달받은 상태                                                                                 |
| 배달 중     | order delivering        | 배달 기사분이 손님에게 배달중인 상태                                                                                      |
| 배달 완료    | order delivery complete | 배달 기사분이 손님에게 전달 완료한 상태                                                                                    |
| 주문 완료    | order complete          | 주문 완료는 매장 직원이 포장 주문이면 손님에게 메뉴 전달 완료한 상황,<br/> 매장 주문이면 매장 손님이 식사 후 계산을 마친 상황, 배달 기사분의 배달 완료를 매장 직원이 확인한 상황 |

## 모델링

- 상품 컨텍스트
  - 상품(Product)
- 메뉴 컨텍스트
  - 메뉴(Menu)
  - 메뉴 그룹(MenuGroup)
- 주문 컨텍스트
  - 매장 주문(EatIn order)
    - 테이블(Ordertable)
  - 포장 주문(Takeout order)
  - 배달 주문(Delivery order)

### 상품
- 속성
  - 반드시 식별자를 가진다.
  - 공백 또는 비속어가 포함되지 않은 이름(name)을 가진다.
  - 반드시 0원 이상의 가격(price)를 가진다.
- 행위
  - 상품 정책에 따라 등록할 수 있다.
    - 상품 등록시 이름과 가격을 정책에 맞게 등록한다.
  - 상품(Product) 가격은 변경될 수 있다.
    - 상품(Product) 가격 변경시 메뉴 가격 정책에 따라 메뉴를 숨길 수 있다.
  - 상품(Product)을 조회할 수 있다.

### 메뉴 그룹
- 속성
  - 반드시 식별자를 가진다.
  - 공백이나 빈값이 들어있지 않은 이름(name)을 가진다.
- 행위
  - 메뉴 그룹(menuGroup)를 정책에 따라 등록할 수 있다.
    - 메뉴 그룹(menuGroup) 등록시 이름 정책에 맞게 등록한다.
  - 메뉴 그룹(menuGroup)를 조회할 수 있다.

### 메뉴
- 속성
  - 반드시 식별자를 가진다.
  - 공백 또는 비속어가 포함되지 않은 이름(name)을 가진다.
  - 반드시 0원 이상의 가격(price)를 가진다.
  - 반드시 하나 이상의 메뉴 그룹(menuGroup)에 속한다.
  - 반드시 하나 이상의 상품을 가진다.
- 행위
  - 메뉴(menu)를 정책에 따라 등록할 수 있다.
    - 메뉴(menu) 등록시 이름과 가격을 정책에 맞게 등록한다.
    - 하나 이상의 메뉴그룹에 속하고, 하나 이상의 상품을 가진다.
  - 메뉴(menu) 가격은 변경될 수 있다.
    - 메뉴(menu) 가격 변경시 가격이 메뉴 상품 가격의 합보다 클 수 없다.
  - 메뉴(menu)를 노출시킬 수 있다.
    - 가격이 메뉴 상품 가격의 합보다 클 수 없다.
  - 메뉴(menu)를 숨길 수 있다.
  - 메뉴(menu)를 조회할 수 있다.

### 테이블
- 속성
  - 반드시 식별자를 가진다.
  - 반드시 공백 또는 비속어가 포함되지 않은 이름(name)을 가진다.
  - 0명 시앙의 손님 수를 가진다.
  - 반드시 빈 테이블 여부를 가진다.
- 행위
  - 테이블은 정책에 따라 등록할 수 있다.
    - 테이블 등록시 이름을 정책에 맞게 등록한다.
  - 빈 테이블을 해지할 수 있다.
  - 빈 테이블을 설정할 수 있다.
    - 주문이 완료된 테이블만 빈 테이블로 설정할 수 있다.
  - 손님 수를 변경할 수 있다.
    - 빈 테이블은 손님 수를 변경할 수 없다.

### 주문
- 속성
  - 반드시 식별자를 가진다.
  - 반드시 주문 타입을 가진다.
  - 반드시 주문 상태을 가진다.
  - 반드시 주문 일자를 가진다.
  - 반드시 하나 이상의 메뉴를 가진다.
    - 반드시 주문한 메뉴의 수량을 가진다.
- 행위
  - 주문은 정책에 따라 등록할 수 있다.
    - 초기 주문 상태는 대기 상태이다.
    - 반드시 하나의 주문 타입을 가진다.
    - 반드시 노출된 메뉴를 선택한다.
      - 주문 항목 가격과 메뉴 가격이 다르면 주문할 수 없다.
    - 주문 상태를 변경할 수 있다.
    - 주문을 조회할 수 있다.

### 배달 주문
- 속성
  - 반드시 배달 주소를 가진다.
  - 주문 메뉴 수량은 0개 이상이다.
- 행위
  - 배달 주문을 정책에 따라 등록할 수 있다.
  - 배달 주문의 주문 상태를 변경할 수 있다.
    - 대기 -> 접수 -> 서빙 -> 배달중 -> 배달 완료 -> 주문 완료
    - 배달 주문이 접수되면 배달 대행사를 호출한다.

### 포장 주문
- 속성
  - 주문 메뉴 수량은 0개 이상이다.
- 행위
  - 포장 주문을 정책에 따라 등록할 수 있다.
  - 포장 주문의 주문 상태를 변경할 수 있다.
    - 대기 -> 접수 -> 서빙 -> 주문완료

### 매장 주문
- 속성
  - 주문 메뉴 수량은 0개 이상이다.
- 행위
  - 매장 주문을 정책에 따라 등록할 수 있다.
    - 빈 테이블인지 확인한다.
  - 매장 주문의 주문 상태를 변경할 수 있다.
    - 대기 -> 접수 -> 서빙 -> 주문 완료
    - 주문 완료되면 빈 테이블로 설정한다.