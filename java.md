# Ubuntu 20.04 에서 openjdk를 11에서 17로 업그레이드 하려면,

# ChatGPT
Ubuntu 20.04에서 OpenJDK를 11에서 17로 업그레이드하는 방법은 다음과 같습니다:

### 1. 기존 JDK 버전 확인
터미널을 열고 현재 설치된 JDK 버전을 확인합니다:
```bash
java -version
```

### 2. 패키지 목록 업데이트
우선 시스템의 패키지 목록을 업데이트합니다:
```bash
sudo apt update
```

### 3. OpenJDK 17 설치
다음 명령어를 사용하여 OpenJDK 17을 설치합니다:
```bash
sudo apt install openjdk-17-jdk
```

### 4. 기본 Java 버전 설정
여러 버전의 JDK가 설치된 경우 기본으로 사용할 버전을 설정할 수 있습니다. 아래 명령어를 사용하여 기본 Java 버전을 설정합니다:
```bash
sudo update-alternatives --config java
```

위 명령을 실행하면 설치된 Java 버전 목록이 표시됩니다. OpenJDK 17을 선택하여 기본 Java로 설정합니다.

### 5. JDK 버전 확인
기본 JDK가 OpenJDK 17로 설정되었는지 확인합니다:
```bash
java -version
```

이 과정을 통해 Ubuntu 20.04에서 OpenJDK를 11에서 17로 업그레이드할 수 있습니다.