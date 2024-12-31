## 목표: 요트 실시간 추적 어플 만들기
streamlit는 python으로 데이터 분석을 위한 웹앱을 쉽게 만들어주는 라이브러리이다.
streamlit 설치방법: vscode -> terminal -> cmd -> pip install streamlit -> streamlit hello -> 자신의 매일로 로그인

대시보드 실행: streamlit run APP.py
지도: folium(추후 구글맵이나 카카오맵으로 변경할예정)
데이터 수신: aisstream.io(AIS), GPS

웹소켓이 뭔지 설명 추가가
양방향 통신: 클라이언트(예: 웹 브라우저)와 서버가 서로 데이터를 주고받을 수 있습니다. 한쪽에서 데이터를 보내면 실시간으로 다른 쪽에서 바로 받을 수 있습니다.

지속적인 연결: 일반적인 HTTP 요청과 달리, 웹소켓 연결은 한번 열리면 클라이언트와 서버 간의 지속적인 연결이 유지됩니다. 이로 인해 실시간 데이터 업데이트가 가능합니다.

낮은 오버헤드: 기존의 HTTP 요청에 비해 데이터 전송 시 헤더가 적어 오버헤드가 낮습니다. 따라서 실시간 데이터를 더 효율적으로 주고받을 수 있습니다.

MMSI를 입력해서 해당 선박의 위치 데이터만 따로 표시가능

개발과정
1. ~~대시보드 생성~~
2. ~~대시보드에 지도 추가~~
3. ~~모의데이터로 위치정보 표시~~
4. ~~streamlit sharing 에서 프로그램 배포해서 URL생성~~ 
5. ~~aisstream.io에 오픈 API신청~~
6. ~~오픈 API를 통해 받은 aisstream.io AIS 데이터 편집~~
7. ~~대시보드 지도에 AIS 위치정보 실시간으로 표시~~
서버를 만들고 거기서 API를 받아와서 지도 상에 표시만 하면됨.
서버를 돌릴떄 실시간 데이터 수집은 계속 돌아가겠끔하고 사용자가 웹에 접근했을때 실시간 데이터 수집을 중지하면서 지도상에 데이터를 표시하게끔 하면됨. 그리고 사용자가 실시간 데이터 수집을 다시 할수있도록 버튼은 그대로 두자자

나중에 우리들이 따로 서버를 만들어서 API를 뿌린다했으니까 일단 모의 데이터를 만들어서 해볼까? 모의 데이터 안에 선박의 길이 너비 같은거나 아니면 선박의 타입을 임의로 입력해서 분류 되게끔 하는거지 아니면 선박의 길이 정보만 있는데 기거서 길이와 너비를 가지고 요트만을 분류한다거나
MMSI를 통해 국적분류

8. 대시보드 디자인, 편의성 다듬기



