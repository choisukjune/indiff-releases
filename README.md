# (indiff) releases

INDIFF 의 설치 파일만 두는 곳입니다. 소스는 여기 없습니다.

설치는 터미널 한 줄로 합니다.

```sh
curl -fsSL https://choisukjune.github.io/indiff-app/install.sh | sh
```

## 업데이트

**0.1.1 부터는 앱이 알려 줍니다.** 새 판이 나오면 앱 안에 알림이 뜨고, 「업데이트」를 누르면
앱이 잠깐 꺼졌다가 새 판으로 다시 켜집니다.

### 수동 업데이트

알림이 뜨지 않는 예전 판(0.1.0)이거나, 앱 안 업데이트가 실패했을 때.

1. INDIFF 를 끕니다 (⌘Q).
2. 터미널에서 설치 한 줄을 다시 실행합니다.

   ```sh
   curl -fsSL https://choisukjune.github.io/indiff-app/install.sh | sh
   ```

3. 같은 자리(`/Applications/INDIFF.app`, 쓸 수 없으면 `~/Applications/INDIFF.app`)에 새 판이 덮어 깔리고 바로 열립니다.
   작업 폴더의 문서는 건드리지 않습니다.

**다른 폴더에 깔아 두었다면** 그 폴더를 알려 줘야 두 벌로 깔리지 않습니다.

```sh
curl -fsSL https://choisukjune.github.io/indiff-app/install.sh | INDIFF_INSTALL_DIR="$HOME/원하는/폴더" sh
```

**지금 판 확인**

```sh
defaults read /Applications/INDIFF.app/Contents/Info CFBundleShortVersionString
```

**DMG 를 브라우저로 받았다면** — 공증하지 않은 앱이라 처음 열 때 「확인할 수 없는 개발자」로 막힙니다.
INDIFF.app 을 응용 프로그램 폴더로 옮긴 뒤 아래 한 줄로 격리 표시를 지우면 열립니다.
(설치 한 줄은 이 표시가 붙지 않아서 이 과정이 필요 없습니다.)

```sh
xattr -dr com.apple.quarantine /Applications/INDIFF.app
```

소개: https://choisukjune.github.io/indiff-app/
