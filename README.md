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
| 한글명 | 영문명 | 설명 |
| --- | --- | --- |
| 상품 | product | 판매할 수 있는 단일 식품 |
| 이름 | name | 상품의 이름 |
| 가격 | price | 상품의 가격(₩) |
| 등록 | create | 포스기에 신규로 상품을 등록한다 |
| 가격 변경 | change price | 등록된 상품의 가격을 변경한다  |

### 메뉴 그룹
| 한글명 | 영문명 | 설명 |
| --- | --- | --- |
| 메뉴 그룹 |  menu group | 메뉴들을 종류에 따라 모아둔 그룹 |
| 이름 | name | 메뉴 그룹의 이름 |
| 등록 | create | 포스기에 신규로 메뉴 그룹을 등록한다 |

### 메뉴
| 한글명 | 영문명 | 설명                      |
| --- | --- |-------------------------|
| 메뉴 | menu | 고객들에게 제공되는 구성품들과 가격의 정보 |
| 이름 | name | 메뉴의 이름                  |
| 가격 | price | 메뉴의 가격(₩)               |
| 구성품 | menu product | 메뉴를 구성하고 있는 상품들         |
| 등록 | create | 포스기에 신규로 메뉴를 등록한다       |
| 활성화 | display | 메뉴를 노출시킨다               |
| 비활성화 | hide | 메뉴를 노출시키지 않는다           |
| 가격 변경 | change price | 등록된 메뉴의 가격을 변경한다        |

### 매장 테이블
| 한글명     | 영문명 | 설명                      |
|---------| --- |-------------------------|
| 매장 테이블  |  order table | 매장 내 고객이 이용할 수 있는 테이블   |
| 이름      | name | 매장 테이블을 지칭하는 이름         |
| 고객 수    | number of guest | 매장 테이블을 이용 중인 인원 수      |
| 이용 중    | occupied | 매장 테이블이 이용 중인 상태        |
| 이용중이 아님 | vacant | 매장 테이블이 이용 되지 않는 상태     |
| 등록      | create | 포스기에 신규로 매장 테이블을 등록한다   |
| 안내      | sit | 고객이 매장테이블을 이용할수 있게 안내한다 |
| 정리      | clear | 매장 테이블을 비운다             |
| 고객 수 변경 | change number of guests | 매장 테이블을 이용중인 인원 수를 변경한다 |

### 주문
| 한글명      | 영문명               | 설명                                      |
|----------|-------------------|-----------------------------------------|
| 주문       | order             | 고객이 선택한 메뉴들                             |
| 배달 주문    | delivery order    | 배달 대행 업체를 통해 음식을 배달하는 형태의 주문            |
| 매장 식사 주문 | eat-in order      | 매장 내에서 식사하는 형태의 주문                      |
| 포장 주문    | takeout order     | 매장에서 포장하여 고객이 외부에서 먹는 형태의 주문            |
| 접수 대기 중  | WAITING           | 주문이 접수되어 사장님/직원분의 수락 대기중인 상태            |
| 수락됨      | ACCEPTED          | 접수된 주문을 포스기를 통해 수락한 상태                  |
| 전달됨      | SERVED            | 매장에서 주문한 구성품이 전달된 상태                    |
| 배달 중     | DELIVERING        | 주문이 배달 중인 상태                            |
| 배달 완료    | DELIVERED         | 배달이 완료된 상태                              |
| 완료됨      | COMPLETED         | 주문에 대한 모든 처리가 완료된 상태                    |
| 배달 대행 업체      | kitchen riders    | 배달기사 배정 및 배달을 대행해주는 업체                  |
| 주문 일자    | order datetime    | 고객이 주문한 날짜와 시간                          |
| 주문 내역    | order line items  | 고객이 주문한 메뉴들                             |
| 배달 요청    | request delivery  | 배달주문이 수락될때 배달 대행 업체에게 배달을 요청한다          |
| 등록       | create            | 고객이 매장에 주문을 한다                          |
| 수락       | accept            | 직원이 접수된 주문을 포스기를 통해 수락한다                |
| 전달       | serve             | 고객이 주문한 구성품을 전달한다                   |
| 배달 시작    | start delivery    | 배달 대행 업체가 배달을 시작한다                      |
| 배달 완료    | complete delivery | 배달 대행 업체가 배달을 완료한다                      |
| 완료       | complete          | 주문에 대한 모든 처리가 끝나, 직원이 포스기를 통해 주문을 완료 한다 |

### 공통
| 한글명 | 영문명       | 설명                                  |
|-----|-----------|-------------------------------------|
| 비속어 | profanity | 욕설이나 부적절한 언어                        |
| 직원  | manager   | 매장에서 근무하는 포스기를 조작 가능한 사장님 혹은 아르바이트생 |

---

## 모델링 (Product)
### 상품(Product)
#### 속성
- `Product` 는 `Price`를 가진다
- `Product` 는 `profanity`가 아닌 `Name`을 가진다

#### 기능
- `Product`를 `Create`할수 있다
- `Product`를 `Change Price`할수 있다
  - `Product`를 `MenuProduct`로 가지고 있는 `Menu`의 `Price`가 `MenuProduct`들의 `TotalPrice`를 넘으면 `Menu`를 `Hide`한다

---

## 모델링 (Menu)
### 메뉴(Menu)
#### 속성
- `Menu`는 `Profanity`가 아닌 `Name`을 가진다
- `Menu`는 `MenuProduct`들의 `TotalPrice`보다 작은 `Price`를 가진다
- `Menu`는 `MenuGroup`을 가진다
- `Menu`는 `MenuProduct`들을 가진다
- `Menu`는 노출 여부인 `display`, `hide`상태를 가진다

#### 기능
- `Menu`는 `Create`할수 있다
- `Menu`는 `Change Price`를 할수 있다
- `Menu`는 `Hide`할수 있다
- `Menu`는 `Display`할수 있다
- `MenuProduct`들의 `TotalPrice`를 계산할수 있다

### 메뉴 그룹(MenuGroup)
#### 속성
- `MenuGroup`은 `Name`을 가진다

### 구성품 (MenuProduct)
#### 속성
- `MenuProduct`는 `Product`를 가진다
- `MenuProduct`는 `Product`의 수량인 `Quantity`를 가진다
- `MenuProduct`는 자신이 포함될 `Menu`를 가진다

---

## 모델링 (EatInOrder)
### 매장 식사 주문(EatInOrder)
#### 속성
- `EatInOrder`는 `Occupied`된 `OrderTable`을 가진다
- `EatInOrder`는 `Order Datetime`을 가진다
- `EatInOrder`는 `Order Line Items`를 가진다

#### 기능
- `EatInOrder`는 `WAITING`, `ACCEPTED`, `SERVED`, `COMPLETED` 순으로 진행된다
- `EatInOrder`가 `COMPLETED`될때, `OrderTable`에 모든 `Order`가 `COMPLETED` 상태라면 `OrderTable`을 `Clean`한다
- `EatInOrder`는 `OrderLineItem`을 취소할 수 있다

### 매장 테이블(OrderTable)
#### 속성
- `OrderTable`은 `Name`을 가지고 있다
- `OrderTable`은 이용중인 `NumberOfGuest`을 가지고 있다
- `OrderTable`은 `Name`을 가지고 있다
- `OrderTable`은 `Occupied`와 `Vacant` 상태를 가질수 있다

#### 기능
- `OrderTable`은 `Clear`할수 있다
- `OrderTable`을 `Occupied`할수 있다
- `OrderTable`은 `Change Number Of Guest`할수 있다

---

## 모델링 (TakeOutOrder)
### 포장 주문(TakeoutOrder)
#### 속성
- `TakeoutOrder`는 `Order Datetime`을 가진다
- `TakeoutOrder`는 `Order Line Items`를 가진다
#### 기능
- `TakeoutOrder`는 `WAITING`, `ACCEPTED`, `SERVED`, `COMPLETED` 순으로 진행된다

---

## 모델링 (DeliveryOrder)
### 배달 주문(DeliveryOrder)
#### 속성
- `DeliveryOrder`는 `DeliveryAddress`를 가진다
- `DeliveryOrder`는 `Order Datetime`을 가진다
- `DeliveryOrder`는 `Order Line Items`를 가진다

#### 기능
- `DeliveryOrder`는 `WAITING`, `ACCEPTED`, `SERVED`, `DELIVERING`, `DELIVERED`, `COMPLETED`순으로 진행된다
- `DeliveryOrder`는 `Kitchen Riders`를 통해 `Start Delivery`해야 한다








