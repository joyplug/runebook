---
layout:	post
title: 	"[mac] iTerm2 & Oh My ZSH"
date: 	2021-11-01 09:00:00 +0900
category: mac
---

## iTerm2 다운로드
[https://iterm2.com/downloads/stable/latest](https://iterm2.com/downloads/stable/latest)   


## XCode Command Line Tool 설치
```shell
sudo xcodebuild -license
agree
```   


## Oh My Zsh 설치
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```


## Oh My Zsh 설정
```bash
vim ~/.zshrc
ZSH_THEME="agnoster"
```


## D2CodingFont 다운로드
[https://github.com/naver/d2codingfont](https://github.com/naver/d2codingfont)


## D2CodingFont 설정
> Spotlight::서체관리자 – D2Coding & D2Coding ligature 붙여넣기  
> VSCode::설정 – Font Family::”D2Coding” – Font Ligature::”D2Coding ligature”  
> VSCode::설정 – Terminal › Integrated: Font Family::”D2Coding”  
> iTerm2::Preferences::Profiles::Text::Font::D2Coding  
> iTerm 종료 & 재실행  


## iTerm2 Color Scheme 다운로드
[https://iterm2colorschemes.com](https://iterm2colorschemes.com)


## iTerm2 Color Preset : ayu 
> ayu 클릭 & 다른 이름으로 저장 시 확장자 .txt 지워주고 실행  
> iTerm2::Preferences::Profiles::Colors::Color Presets::ayu  
> iTerm2::Preferences::Appearance::General::Theme::Minimal  


## iTerm2 셋업 
```bash
vim ~/.zshrc
prompt_context() {
  if [[ "$USER" != "$DEFAULT_USER" || -n "$SSH_CLIENT" ]]; then
    prompt_segment black default "%(!.%{ % F {yellow}%}.)$USER"
  fi
}
source ~/.zshrc
```
-> F전후 공백 지워서 복사하여 사용!


## Homebrew 설치 
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/joyplug/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```


## Oh My Zsh Prettier 셋업 
```bash
brew install zsh-syntax-highlighting
source /opt/homebrew/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
 
vim ~/.zshrc
source /opt/homebrew/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```
