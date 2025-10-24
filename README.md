
# 🛒 MM Process 담당 – 이지은

## 📦 프로젝트 개요

본 프로젝트는 SAP ABAP 기반 ERP 시스템으로,
구매–입고–회계–판매 프로세스를 통합 관리하기 위해 개발되었습니다.
저는 MM(Material Management) 영역을 담당하여,
구매 오더부터 입고 처리, 납품 성실도 분석까지의 전체 흐름을 설계 및 구현했습니다.

## ⚙️ 담당 업무

| 프로그램명                   | 유형          | 주요 기능                                     |
| ----------------------- | ----------- | ----------------------------------------- |
| **구매 오더 관리 프로그램**       | Module Pool | 구매 오더 생성, 조회, 수정 및 삭제 / 대량 업로드 기능(BDC) 지원 |
| **구매 오더 승인 프로그램**       | Module Pool | 관리자 승인 프로세스 구현 |
| **입고 프로그램**  | Module Pool | 승인된 오더 기준 입고 처리 및 입고문서 자동 생성              |
| **벤더사별 납품 성실도 분석 프로그램** | Report      | 납기일 대비 입고일을 기준으로 납품 정확도(%) 산출 및 성실도 등급 표시 |
| **상품 마스터 관리 프로그램**      | Module Pool | 상품 정보 생성, 조회, 수정 및 삭제 구현     |


## 🧩 구현 포인트

* **구매–입고–회계 간 데이터 흐름을 연결**

  * 구매 오더 생성 → 승인 → 입고 → 송장 연계로 이어지는 MM–FI 통합 구조 설계
* **사용자 편의성 강화**

  * BDC 엑셀 업로드로 대량 구매오더 생성
  * ALV Grid를 활용한 상태별 시각화 (신호등, 합계행, 셀 색상 강조)

* **모듈 간 일관성 유지**

  * FI(회계) 모듈과의 데이터 연동 고려하여 PO–GR–IV 데이터 정합성 확보


## 🖥️ 시연 화면

### 🎬 구매 오더 생성, 승인, 입고 흐름 - 시연영상 

>  [PO & PO Approval & GR Demo](https://drive.google.com/drive/folders/1y8UHAi1-6cTIWlsWPiLzIe7yebxeMFV7?usp=sharing)

### 시연 캡처 화면
#### 구매오더 조회 및 생성
<img width="1474" height="1243" alt="PO조회생성" src="https://github.com/user-attachments/assets/55113f67-bee6-49c9-b6a7-0bb39a44bccf" />

#### 구매오더 변경 및 상세조회
<img width="1404" height="1233" alt="PO변경조회" src="https://github.com/user-attachments/assets/83d88e7f-6961-411a-85e2-e9168522cbfa" />

#### 구매오더 승인 및 반려
<img width="1465" height="1240" alt="PO승인반려" src="https://github.com/user-attachments/assets/77d2107d-40e9-4f99-bd66-9bb673d83be5" />

#### 입고
<img width="1480" height="1239" alt="입고" src="https://github.com/user-attachments/assets/03127528-58b0-4e32-ae8a-81747ccf41f3" />



## 💬 기술 스택

| 구분          | 사용 기술                                      |
| ----------- | ------------------------------------------ |
| **언어**      | ABAP                                       |
| **프로그램 유형** | Module Pool / Report                       |
| **UI 구성요소** | ALV Grid, Search Help, Subscreen, Popup    |
| **데이터 관리**  | Custom Table (ZTPBPOH, ZTPBPOI, ZTPBGRH 등) |
| **프로세스 연계** | PO → GR → IV (FI 연동)                       |


## 🌱 느낀 점

SAP ERP의 MM 프로세스를 직접 구현하면서,
업무 흐름의 표준화와 데이터 정합성의 중요성을 체감했습니다.
특히 사용자 입장에서 프로그램을 설계하는 것이 얼마나 중요한지 배우며,
“편리하면서도 안정적인 ERP 프로세스”를 구현하는 개발자의 역할을 깊이 이해했습니다.

