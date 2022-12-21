## ⚠️ 사용 전 확인

1. https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification에서
2. gtzan-dataset-music-genre-classification.zip 파일을 다운 받고
3. python-files 내에 저장
4. index.js 또는 웹 실행

1~2의 과정은 music-classification 폴더의 music-classification.ipynb 파일을 실행하면 아이디 없이 설치가 가능

# Genre Surf User Interface

## 음악 장르 분류 및 곡 추천 웹 프로젝트 서버

### 🚀 프로젝트 설명

이 프로젝트는 음악 장르 분류를 통한 곡 추천 웹 프로젝트입니다.

이 폴더는 프로젝트의 서버를 담고 있습니다.

클라이언트에서 장르 분류 요청과 함께 입력된 오디오 파일에 대한 처리를 하는 API를 제공합니다.

입력된 오디오 파일은 `uploads` 폴더에 저장하고, 이 파일을 Python 오디오 특성 추출 파일(`python-files/audioFeat`)의 매개변수로 전달하고 해당 파일을 실행합니다.

Python 오디오 특성 추출 파일로부터 오디오 특성을 받고, 이 데이터는 다시 Python 장르 분류 파일(`python-files/predictGenre.py`)의 매개변수로 전달하고 해당 파일을 실행합니다.

Python 장르 분류 파일로부터 받은 장르명은 클라이언트에게 전달합니다.

클라이언트에서 해당 장르명에 대한 유튜브 웹 크롤링을 요청하면, 서버에서 해당 장르명을 Python 유튜브 웹 크롤링 파일(`python-files/youtubeCrawler.py`)의 매개변수로 전달하고 해당 파일을 실행합니다.

해당 파일에서는 해당 장르명을 기반으로 한 검색 결과 내에서 24시간 이상 재생할 수 있는 재생목록을 생성하고 재생합니다.

모두 재생이 끝나면 총 재생 시간을 클라이언트에게 전달합니다.

### ⚠️ 프로젝트 시작 전!

```
npm install
```

을 통해 필요한 모듈을 설치해주세요.

```
nodemon index.js
```

모듈이 모두 설치 되었으면 위 명령어를 통해 웹프로젝트의 서버를 `http://localhost:8080/`에서 실행할 수 있게 됩니다.
