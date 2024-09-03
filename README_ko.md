# FileContentExtractor

**언어:** [🇺🇸English](README.md) | [🇰🇷한국어](README_ko.md)

`FileContentExtractor`는 디렉토리 내의 텍스트 파일 내용을 재귀적으로 추출하여 저장하는 다기능 Python 도구입니다. 특정 파일이나 디렉토리를 무시하고, 여러 기준에 따라 파일을 필터링하며, 파일 경로를 절대 경로나 상대 경로로 출력할 수 있는 다양한 옵션을 제공합니다. 또한 사용자 확인, 버전 정보 표시, 도움말 옵션을 포함하여 사용성을 높였습니다.

## 주요 기능

- 디렉토리를 재귀적으로 탐색하여 텍스트 파일 내용을 추출합니다.
- `.ignorelist` 파일을 사용하여 특정 파일, 디렉토리 또는 패턴을 무시할 수 있습니다.
- 파일 경로를 상대 경로나 절대 경로로 출력할 수 있습니다.
- 파일 확장자, 크기, 수정 날짜를 기준으로 파일을 필터링할 수 있습니다.
- 출력 파일을 크기 기준으로 여러 개로 나눌 수 있습니다.
- 추출 진행 상황을 표시하는 진행 바를 제공합니다.
- 추출을 진행하기 전에 사용자 확인을 요청합니다.
- 커맨드라인 옵션을 통해 버전 정보와 도움말 세부 정보를 제공합니다.

## 설치

`pip`를 통해 패키지를 설치할 수 있습니다:

```bash
pip install file-content-extractor
```

## 사용법

1. **기본 명령어**:

   - 기본 사용 (상대 경로 출력):

     ```bash
     file_extractor
     ```

     - 이 명령어를 실행한 후, 추출을 확인하는 메시지가 표시되며, `y`를 입력해야만 진행됩니다.

   - 절대 경로 사용:

     ```bash
     file_extractor -a
     ```

2. **추가 옵션 지정**:

   - 특정 파일이나 디렉토리 무시:

     ```bash
     file_extractor -i my_ignore_list.txt
     ```

   - 출력 파일을 사용자 지정 파일로 저장:

     ```bash
     file_extractor -o my_output.txt
     ```

   - 파일 확장자, 크기, 수정 날짜로 필터링:

     ```bash
     file_extractor -e .txt,.py -m 1024 -M 1048576 -d 2023-01-01
     ```

   - 출력 파일을 여러 개로 나누기:

     ```bash
     file_extractor -s 10485760
     ```

   - 추출을 시작할 디렉토리 지정:

     ```bash
     file_extractor -p /path/to/directory
     ```

3. **버전 확인**:

   - 도구의 현재 버전을 확인하려면:

     ```bash
     file_extractor -v
     ```

4. **도움말**:

   - 사용법 정보와 옵션 세부 사항을 보려면:

     ```bash
     file_extractor -h
     ```

## 옵션

- `-a`, `--absolute`: 출력에서 절대 경로를 사용합니다.
- `-i <file>`, `--ignore=<file>`: 사용자 지정 무시 파일을 지정합니다 (기본값은 `.ignorelist`).
- `-o <file>`, `--output=<file>`: 사용자 지정 출력 파일을 지정합니다 (기본값은 `output.txt`).
- `-e <ext1,ext2,...>`, `--extensions=<ext1,ext2,...>`: 포함할 파일 확장자를 지정합니다 (예: `.txt,.py`).
- `-m <bytes>`, `--min-size=<bytes>`: 포함할 최소 파일 크기를 지정합니다.
- `-M <bytes>`, `--max-size=<bytes>`: 포함할 최대 파일 크기를 지정합니다.
- `-d <YYYY-MM-DD>`, `--modified-after=<YYYY-MM-DD>`: 특정 날짜 이후에 수정된 파일만 포함합니다.
- `-s <bytes>`, `--split-size=<bytes>`: 지정된 크기로 출력 파일을 나눕니다.
- `-p <directory>`, `--path=<directory>`: 추출을 시작할 디렉토리를 지정합니다.
- `-h`, `--help`: 이 도움말 메시지를 표시하고 종료합니다.
- `-v`, `--version`: 버전 정보를 표시하고 종료합니다.

## 기여

기여는 언제나 환영입니다! 자유롭게 Pull Request를 제출해 주세요.

## 라이선스

이 프로젝트는 MIT 라이선스에 따라 배포됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## 작성자

- **Daniel** - [joonheeu](https://github.com/joonheeu) - daniel@udit.one
- **회사**: UDIT