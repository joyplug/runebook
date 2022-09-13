---
layout: post
title:  "[minecraft] 마인크래프트 플러그인"
date:   2021-11-13 09:00:00 +0900
category: minecraft
---

## 0. EssentialX
> [https://dev.bukkit.org/projects/essentialsx](https://dev.bukkit.org/projects/essentialsx)   
> [https://dev.bukkit.org/projects/essentialsx/files/3445258#additional-files](https://dev.bukkit.org/projects/essentialsx/files/3445258#additional-files)


## 1. LuckPerms //권한 관리 플러그인
> [https://luckperms.net/download](https://luckperms.net/download)   
> [https://dev.bukkit.org/projects/vault/files](https://dev.bukkit.org/projects/vault/files)
```shell
- plugins 폴더에 복사
- /lp help
- /lp creategroup admin | vip | default(newbie)
- /lp listgroups
- /lp group default rename newbie
- /lp listgroups
- /lp user DL_linza parent set admin
- /lp group admin meta addprefix 1(우선순위) "[어드민]"
- 채팅 시 닉네임 앞에 칭호 확인
- /lp group admin meta removeprefix 1
- /lp group admin meta addsuffix 1 "::"
- /lp group admin meta removesuffix 1
- /lp group newbie permission set essentials.spawn
- /lp group newbie permission unset essentials.spawn
- /lp editor : 링크를 브라우저에서 편집하기  (essentials.sethome, essentials.tpa,...)
- /lp applyedits###### : 편집 종료 시 마크 채팅창에 붙여넣기
```


## 2. 서버 여러 버전 접속하게 만들기 (ProtocolSupport/스피곳 전용)
> [https://www.spigotmc.org/resources/protocolsupport.7201](https://www.spigotmc.org/resources/protocolsupport.7201)


## 3. WorldEdit
```shell
//wand
Left click & Right click
//set 1(stone)
//undo
//set 57(diamond)
//walls 57 <-벽만
//outline 57 <-윤곽선만
//cyl 57 7 12 <- 반지름 7, 높이 12 다이아몬드 속찬 원기둥
//hcyl 46(TNT) 10 5
//up 10  <-10블록 위로 블록 생성
//sphere 155 13 <-속 꽉찬 구
//hsphere 155 6 <- 속이 빈 구
```


## 4. Holographic Displays
> [https://dev.bukkit.org/projects/holographic-displays/files](https://dev.bukkit.org/projects/holographic-displays/files)


## 5. AutoPickup
> [https://dev.bukkit.org/projects/autopickup/files](https://dev.bukkit.org/projects/autopickup/files)
```shell
- LuckPerms 시
AutoPickup.enabled :: 자동으로 아이템 줍기
AutoBlock.enabled :: 광물이 자동 블록화
AutoSmelt.enabled :: 광물이 자동으로 구워지기
AudoSell.enabled :: 광물이 자동으로 판매되는 것을 활성화 (QuickSell 플러그인 필요)
AutoPickup.BlockGui :: 오토픽업 플러그인 GUI 막기
AudoPickup.infinity :: 도구의 내구도가 줄어드는 것을 방지
- /autopickup  <- 초록색인 경우 On
```


## 6. ChestCommandsGUI
> [https://dev.bukkit.org/projects/chest-commands/files](https://dev.bukkit.org/projects/chest-commands/files)
```shell
- 압축해제 시 jarfile & ChestCommands folder
- server/plugins 에서 복사
- server/plugins/ChestCommands/menu/example.yml
- notepad++ 설치
- name : 체스트 커맨드 이름
- rows : 체스트 커맨드의 줄 수
- command : '실험'   <- /실험 치면 체스트커맨드가 열림
- open-action: 'tell: &e메뉴를 열었습니다.'   <- 체스트커맨드 열었을때 뜨는 채팅메시지
- open-with-item:
id: 369  (블레이즈 막대기)
left-click: false (좌클릭시 열림)
right-clieck: true  (우클릭시 열림)
- ex) 스폰가기: 아침으로: 밤으로: 누르면죽음:
COMMNAD: 'spawn' / 'time set day' / 'time set night' / '죽기'
NAME: '&e&l스폰으로 이동하기!'
LORE: '&f클릭하시면 스폰으로 이동합니다.'
ID: 381 (엔더눈)
POSITION-X: 2
POSITION-Y: 2
>chestcommands reload
```


## 7. BanItem
> [https://dev.bukkit.org/projects/banitem](https://dev.bukkit.org/projects/banitem)
```shell
- /banitem add 티엔티 <- 아이템 손에 들고 입력
- /banitem del <- 아이템 손에 들고 입력
```


## 8. AutoSaveWorld
> [https://dev.bukkit.org/projects/autosaveworld/files](https://dev.bukkit.org/projects/autosaveworld/files)
```shell
- plugins/AutoSaveWorld/config.yml
- notepad++
- backup: localfs: destinationfolders: 컴퓨터백업경로
- save: interval: 900 (초단위)
- backup: interval
- /save
- /backup
```


## 9. TabList
> [https://www.spigotmc.org/resources/animated-tab-tablist.46229](https://www.spigotmc.org/resources/animated-tab-tablist.46229)
```shell
- 압축 푼 jar file && TabList folder를 plugins에 복사
- Tab키를 눌러봄
- plugins/TabList/animcreator.yml
- notepad++
- /tablist rl
```


## 10. PixelPrinter
> [https://dev.bukkit.org/projects/pixelprinter/files](https://dev.bukkit.org/projects/pixelprinter/files)
```shell
- server/plugins/PixelPrinter/images/  <- 사진넣기
- /pp help
- /pp specs [파일이름]
- /pp create [방향] [파일이름] [높이 | 100블록?]
:: 해당 사진을 [방향] 쪽으로 맵에 출력합니다.
:: 높이가 높을수록 퀄리티가 높아집니다.
- ​/pp cf [방향] [파일이름] [높이]
:: 해당 사진을 [방향] 쪽으로 맵에 액자 사진을 생성합니다. 
- /pp createskin [방향] [플레이어이름 or UUID]
:: 해당 플레이어의 스킨의 동상을 [방향] 쪽으로 생성합니다. (UUID 사용 가능)
- /pp stopAllGifs
:: 서버 내에 있는 모든 GIF(움짤) 출력물의 재생을 멈춥니다.
- /pp delete [파일이름]
:: plugins 폴더 > PixelPrinter 폴더 > images 폴더에 있는 해당 사진을 삭제합니다.
- East / North /  South /  North /  FlatNorthEast, FlatNorthWest /  FlatSouthEast / FlatSouthWest
- 삭제할때는 worldedit 플러그인 //wand && LeftRight click && //cut
```
