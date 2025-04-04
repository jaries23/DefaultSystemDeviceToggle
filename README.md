# 🎧 SoundDeviceSwitcher

> 🔽 English instructions are available below.

Windows에서 두 개의 오디오 장치(예: 이어폰과 스피커)를 **스마트하게 전환**할 수 있는 배치 스크립트입니다.

단순한 토글이 아닌, 다음과 같은 **지능적인 기능**을 제공합니다:

- ✅ **두 장치가 모두 연결된 경우에만 전환 실행**
- 🔁 현재 기본 장치를 확인한 뒤 **다른 장치로 자동 전환**
- 🔊 **기본 재생 장치**와 **기본 통신 장치**를 동시에 설정
- 🔔 전환 후 트레이 알림으로 상태 표시
- ⚡ Stream Deck, AutoHotKey 등 **단축키 도구와 연동** 용이

> 💡 장치가 하나라도 연결되어 있지 않으면, 스크립트는 전환을 취소하고 경고 메시지를 표시합니다.

---

## ✅ 사용 방법 (Korean)

### 1. NirCmd 다운로드
- 공식 사이트: https://www.nirsoft.net/utils/nircmd.html  
- 페이지 하단에서 **“NirCmd 64-bit”** 다운로드  
- 압축 해제 경로: `C:\Program Files\nircmd-x64`  
- 폴더 안에 `nircmd.exe`가 있어야 합니다

### 2. 시스템 환경 변수 등록
- 시작 메뉴에서 “시스템 환경 변수 편집” 검색 후 실행  
- 아래 순서대로 진행:  
  - "환경 변수(N)..." 클릭  
  - 시스템 변수에서 `Path` 선택 → "편집(I)..." 클릭  
  - "새로 만들기(N)" → `C:\Program Files\nircmd-x64` 입력  
  - 모든 창을 "확인"으로 닫기

### 3. PowerShell 오디오 모듈 설치 (최초 1회만)
- `Win + R` → `powershell` 입력 후 Enter  
- 아래 명령어를 복사하여 붙여넣고 실행:
  ```powershell
  Install-Module -Name AudioDeviceCmdlets -Scope CurrentUser -Force
  ```
- 설치 중 저장소 신뢰 여부를 묻는 경우 `Y` 입력 후 Enter

### 4. 오디오 장치 이름 설정
- `device.bat` 파일의 확장자를 `.txt`로 바꿔 메모장으로 열기  
- `[설정]` 항목 아래의 `earphone`, `speaker` 값에 본인의 장치 이름 입력  
- 저장 후 닫고, 확장자를 다시 `.bat`로 변경  

---

## ✅ How to Use (English)

**SoundDeviceSwitcher** is a batch script for **smartly toggling** between two audio devices on Windows (e.g., headphones and speakers).

It’s more than just a toggle—this script includes intelligent features:

- ✅ **Only switches if both devices are connected**
- 🔁 Automatically detects the current default device and switches to the other
- 🔊 Sets both the **Default Playback Device** and **Default Communication Device**
- 🔔 Displays a tray notification after switching
- ⚡ Easily integrates with hotkey tools like Stream Deck or AutoHotKey

> 💡 If either device is not connected, the script will cancel the operation and show a warning instead of switching.

---

### 1. Download NirCmd
- Official site: https://www.nirsoft.net/utils/nircmd.html  
- Scroll to the bottom and download **"NirCmd 64-bit"**  
- Extract to: `C:\Program Files\nircmd-x64`  
- Make sure `nircmd.exe` is in that folder

### 2. Add to System Environment Variables
- Open the Start menu and search for “Edit the system environment variables”  
- In the window:  
  - Click “Environment Variables...”  
  - Under "System variables", select `Path` → click “Edit...”  
  - Click “New” → add: `C:\Program Files\nircmd-x64`  
  - Click OK to close all windows

### 3. Install PowerShell Audio Module (one-time setup)
- Press `Win + R`, type `powershell`, then press Enter  
- Paste and run the following command:
  ```powershell
  Install-Module -Name AudioDeviceCmdlets -Scope CurrentUser -Force
  ```
- If prompted about trusting the repository, type `Y` and press Enter

### 4. Set Your Audio Device Names
- Rename `device.bat` to `.txt` and open it in Notepad  
- Under the `[설정]` section, enter your actual device names for `earphone` and `speaker`  
- Save and close the file, then rename the extension back to `.bat`

---
