# 🍈 Mp3tag Melon Web Source

![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![ID3 Version](https://img.shields.io/badge/ID3-v2.3-orange?style=flat-square&logo=tag)

| Platform | Windows | macOS |
| :---: | :---: | :---: |
| **OS** | ![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=flat-square&logo=windows&logoColor=white) | ![Platform](https://img.shields.io/badge/Platform-macOS-000000?style=flat-square&logo=apple&logoColor=white) |
| **Mp3tag** | ![Mp3tag Version](https://img.shields.io/badge/Mp3tag-v3.22%2B-blue?style=flat-square&logo=tag) | ![Mp3tag Version](https://img.shields.io/badge/Mp3tag-v1.82%2B-black?style=flat-square&logo=tag) |

[Melon(멜론)](https://www.melon.com)의 음원 데이터를 파싱하여 [Mp3tag](https://www.mp3tag.de/en)에서 앨범 및 곡 정보를 손쉽게 정리할 수 있는 웹 소스 스크립트입니다.

> ⚠️ **주의**: 본 스크립트는 공식 API가 아닌 **웹 HTML 파싱** 방식을 사용합니다. 멜론 웹페이지 구조가 변경될 경우 일시적으로 작동하지 않을 수 있습니다.

---

## 📦 설치 방법

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/stellarhyeok/Mp3tag-Melon-source?logo=github)](https://github.com/stellarhyeok/Mp3tag-Melon-source/releases)

1. [Mp3tag](https://www.mp3tag.de/en/download.html) 최신 버전을 설치합니다.
2. `Mp3tag-Melon-source.zip`의 압축을 풀고 `.src`, `.inc`, `.settings` 파일들을 아래 경로에 붙여넣으세요.

### ⚡ 가장 쉬운 방법 (공통)
Mp3tag 실행 후 메뉴에서 아래 경로를 엽니다.
> **파일 > 구성 폴더 열기 > (폴더) > data > sources**

### 🪟 Windows (Manual)
```
%appdata%\Mp3tag\data\sources\
```

### 🍎 macOS (Manual)
```
~/Library/Application Support/Mp3tag/data/sources/
```

---

## 🚀 사용 가이드

### 1. 앨범 검색
> ℹ️ **Note**: 검색 결과는 **최대 21개**까지 출력됩니다. 검색 결과가 하나인 경우, 태그 수정창이 표시됩니다.

**[검색 결과 화면]**

| (Cover) | Album | Artist | Title | Released | Tracks |
|:---:|:---|:---|:---|:---:|:---:|
| 마우스 오버 시 확대 | 앨범 이름 | 앨범 아티스트 | 타이틀 곡 | 발매일 | 트랙 수 |

* **미리보기**: 결과 항목 클릭 시 멜론 앨범 상세 페이지로 이동

**[태그 수정 필드 (Tag Mapping)]**

| 필드명 (ID3v2.3) | 태그 설명 | 비고 |
|:---:|:---|:---|
| `ALBUM` | 앨범 이름 | |
| `ALBUMARTIST` | 앨범 아티스트 | |
| `TITLE` | 곡 이름 | |
| `ARTIST` | 곡 아티스트 | |
| `TRACK` | 트랙 번호 | |
| `DISCNUMBER` | 디스크 번호 | |
| `PUBLISHER` | 발매사 | |
| `YEAR` | 발매년도 | 설정에 따라 날짜 포맷 변경 |
| `COVER` | 앨범 아트 | **Max 1000px** |


### 2. 곡 검색
> ℹ️ **Note**: 검색 결과는 **최대 50개**까지 출력됩니다. 검색 결과가 하나인 경우, 태그 수정창이 표시됩니다.

**[검색 결과 화면]**

| Title | Artist | Album |
|:---|:---|:---|
| 곡 이름 | 곡 아티스트 | 앨범 이름 |

* **미리보기**: 결과 항목 클릭 시 멜론 곡 상세 페이지로 이동

**[태그 수정 필드 (Tag Mapping)]**

| 필드명 (ID3v2.3) | 태그 설명 | 비고 |
|:---:|:---|:---|
| `TITLE` | 곡 이름 | |
| `ARTIST` | 곡 아티스트 | |
| `ALBUM` | 앨범 이름 | |
| `GENRE` | 장르 | |
| `COMPOSER` | 작곡가 | |
| `LYRICIST` | 작사가 | |
| `YEAR` | 발매년도 | 설정에 따라 날짜 포맷 변경 |
| `UNSYNCEDLYRICS` | **비동기 가사** | |
| `COVER` | 앨범 아트 | **Max 1000px** |

---

## ⚙️ 설정 (s. 설정)

스크립트 동작을 제어할 수 있습니다.

### 발매일 형식
- ✅ **Check**: `20220101` (YYYYMMDD 형식)
- ⬜ **Uncheck**: `2022` (YYYY 형식, 기본값)

### 줄바꿈 호환성
- ✅ **Check (Mac용)**: 가사 출력 시 **macOS** 형식(`\n`) 줄바꿈 사용
- ⬜ **Uncheck (Windows용)**: 가사 출력 시 **Windows** 형식(`\r\n`) 줄바꿈 사용 (기본값)

---

## 🔗 참고 자료 (References)

- [Mp3tag Web Sources Documentation](https://docs.mp3tag.de/tag-sources/development/)
- [Original Concept & Reference (Naver Blog)](https://blog.naver.com/hosang46/221126952898)