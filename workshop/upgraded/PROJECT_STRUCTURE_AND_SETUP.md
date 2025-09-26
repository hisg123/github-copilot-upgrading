# upgraded 디렉터리 구조 및 설정 안내

이 디렉터리는 legacy 코드의 복사본을 기반으로 Python 최신 버전 호환성 및 현대화 작업을 진행하는 공간입니다.

## 디렉터리 구조

- MANIFEST.in
- README.rst
- distribute-0.6.10.tar.gz
- distribute_setup.py
- docs/
- guachi/
- guachi.egg-info/
- setup.py

## 설정 파일 예시 (pyproject.toml)

아래는 현대 Python 프로젝트 표준에 맞춘 예시 설정 파일입니다. 실제 프로젝트에 맞게 수정해 사용하세요.

```toml
[build-system]
requires = ["setuptools>=61.0", "wheel"]
build-backend = "setuptools.build_meta"

[project]
name = "guachi-upgraded"
version = "0.1.0"
description = "Modernized version of legacy guachi project."
authors = [
  { name="Your Name", email="your@email.com" }
]
readme = "README.rst"
requires-python = ">=3.8"
dependencies = [
  "pytest",
  "sqlite3"
]

[tool.pytest.ini_options]
testpaths = ["guachi/tests"]
```

- 필요에 따라 `setup.cfg` 또는 기타 설정 파일을 추가할 수 있습니다.
- 실제 의존성 및 Python 버전은 프로젝트 상황에 맞게 조정하세요.
