
# DART-Disclosure-Summarizer

**NLP DART 프로젝트**는 Open DART 시스템에서 제공하는 공시 정보를 자동으로 다운로드하고, 이를 자연어 처리(NLP)를 통해 요약하는 Python 기반의 프로젝트입니다.  
사용자는 기업명과 기간을 입력하여 해당 기간 동안의 공시를 자동으로 다운로드하고 요약할 수 있습니다.

---

## 설치 방법

1. **가상 환경 생성 및 활성화**

2. **필요한 패키지 설치**

   ```bash
   pip install -r requirements.txt
   ```

---

## 사용법
NLP DART.ipynb에서 순서대로 셀을 실행하면 됩니다.

## 주요 기능

- **기업 검색**: 사용자가 입력한 회사명으로 기업을 검색하고 선택할 수 있습니다.
- **공시 다운로드**: DART API를 통해 지정된 기간의 공시를 ZIP 파일로 다운로드합니다.
- **NLP 요약**: 두 개의 NLP 모델을 사용하여 공시 내용을 요약하고, 결과를 결합합니다.

---

## 사용된 모델

- **`lcw99/t5-base-korean-text-summary`**: 메인 요약에 사용
  https://huggingface.co/lcw99/t5-base-korean-text-summary
- **`psyche/KoT5-summarization`**: 보조 요약에 사용
  https://huggingface.co/psyche/KoT5-summarization

---

## 프로젝트 구조

```bash
NLP_DART/
│-- NLP DART.ipynb              # 메인 Jupyter Notebook 파일
│-- requirements.txt            # 의존성 패키지 목록
│-- download/                   # 다운로드된 공시 파일 저장 폴더
│-- README.md                   # 프로젝트 설명 파일
```

---

## 참고 사항

### DART API Key

공시를 다운로드하기 위해서는 DART API 키가 필요합니다.  
DART OpenAPI에서 발급받은 API 키를 코드에 설정하세요.

### 환경 설정

- **Python 버전**: 3.11 이상
- 가상 환경 사용을 권장합니다.
