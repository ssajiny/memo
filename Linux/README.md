## 계정 생성
### 1. 계정 생성
사용자 이름이 USERNAME인 새 사용자 생성
```
sudo useradd [OPTIONS] USERNAME
```
옵션 없이 실행되면 useradd는 /etc/default/useradd 파일에 지정된 기본 설정을 사용하여 새 사용자 계정을 만든다.
명령은 /etc/passwd, /etc/shadow, /etc/group 및 /etc/ghadow 파일에 항목을 추가한다.

### 2. 암호 설정
새로 만든 사용자로 로그인하려면 사용자 암호를 설정해야 한다.
```
sudo passwd sangjin
```

### 3. 그룹 설정
먼저 그룹을 생성한다.
```
groupadd mygroup
```

생성한 그룹에 계정을 추가한다.
```
usermod -G mygroup sangjin
```

### 4. 계정 변경

```
su sangjin
```
현재 계정 정보 확인
```
# whoami
```
