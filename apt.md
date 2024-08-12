# apt update

* [Ubuntu apt - the repository '...' does not have a release file.](https://velog.io/@dbadoy/Ubuntu-apt-Release-does-not-have-a-Release-file)

# Error
`sudo apt update` 명령어를 실행할 때 404 Not Found 에러가 발생하는 경우, 다음 사항들을 확인해야 합니다:

1. **소프트웨어 소스 (리포지터리) URL 확인**:
   - `404 Not Found` 에러는 주로 `/etc/apt/sources.list` 파일이나 `/etc/apt/sources.list.d/` 디렉터리 내의 파일에 잘못된 리포지터리 URL이 설정되어 있을 때 발생합니다. 
   - 명령어를 실행하여 현재 설정된 리포지터리 목록을 확인할 수 있습니다.
     ```bash
     cat /etc/apt/sources.list
     cat /etc/apt/sources.list.d/*.list
     ```
   - 각 URL이 올바른지, 더 이상 지원되지 않는 리포지터리를 참조하고 있지 않은지 확인하세요.

2. **리포지터리 상태 확인**:
   - 참조 중인 리포지터리가 폐쇄되었거나 주소가 변경되었을 수 있습니다. 해당 리포지터리의 공식 웹사이트나 관련 문서를 통해 주소가 변경되었는지 확인하세요.
   
3. **배포판 코드네임 확인**:
   - 특정 배포판의 코드네임이 변경되었을 경우, `sources.list` 파일 내에서 사용하는 코드네임이 올바른지 확인해야 합니다. 예를 들어, Ubuntu에서 `bionic`, `focal` 등 코드네임이 올바르게 설정되어 있는지 확인합니다.

4. **네트워크 문제**:
   - 네트워크 문제로 인해 리포지터리에 접근하지 못할 수도 있습니다. 인터넷 연결 상태를 확인하고, 해당 리포지터리가 웹 브라우저에서 접속 가능한지 확인하세요.

5. **Proxy 설정 확인**:
   - 만약 프록시 서버를 사용하고 있다면, 프록시 설정에 문제가 있어 리포지터리에 접근하지 못할 수도 있습니다. 이 경우, `/etc/apt/apt.conf` 파일을 확인하여 프록시 설정이 올바르게 되어 있는지 확인하세요.

이러한 확인 작업을 거쳐 문제를 해결할 수 있습니다. 문제가 지속될 경우, 특정 에러 메시지를 기반으로 추가적인 조치를 취해야 할 수도 있습니다.