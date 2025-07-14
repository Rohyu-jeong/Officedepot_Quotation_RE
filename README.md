# 견적서 메일 자동화 프로그램

> **작업 지시서의 품목 데이터를 바탕으로 오피스디포에서 견적서를 생성하고 이를 PDF로 저장 후 메일로 전송하는 자동화 프로그램입니다.**

<br>

## 기술 환경

- UiPath Studio  
- Robotic Enterprise Framework (REFramework)  
- Excel, PDF, Web Automation  
- HTML Email, DataTable, Dictionary 등 활용  

<br>

## 자동화 흐름 요약

1. 메일로 수신된 작업 지시서를 확인하고, 구매처(오피스디포, 드림디포 등)별로 구분  
2. 구매처에 따라 해당 쇼핑몰 사이트에 접속  
3. 작업 지시서에 포함된 품목 코드와 수량을 기준으로 상품을 검색  
4. 검색 결과 중 일치하는 품목을 식별하여 상세 페이지에 접속  
5. 장바구니에 해당 품목을 추가  
6. 모든 품목을 장바구니에 담은 후, 장바구니 페이지에서 견적서 PDF 저장  
7. 저장된 PDF에서 품목 코드 및 수량 정보 추출  
8. 원본 지시서와 PDF 내 데이터 비교 후 불일치 항목 및 수량 일치 여부를 검증  
9. 최종 검증이 완료된 메일만 본문을 작성하고, 견적서를 첨부하여 메일 발송  

<br>

## Workflow 구성

- **Initialization** <br>
  01\_폴더 초기화.xaml <br>
  02\_메일 수신 및 첨부파일 저장.xaml <br>
  03\_구매처 목록 추출.xaml <br>
  04\_Transaction DT 생성.xaml <br>

- **Process Transaction** <br>
  05\_구매처 DT 변환.xaml <br>
  06\_견적서 생성.xaml <br>
  07\_견적서 PDF 이동.xaml <br>
  08\_견적서 검증.xaml <br>

- **End Process** <br>
  09\_메일 발송.xaml <br>
