---
layout: post
title: TypeScript 블록체인 만들기; 개발세팅
categories:
  - js
tags:
  - TypeScript
  - JavaScript
excerpt_separator:  <!--more-->

---

### 1. typescript 및 tsc-watch 설치
```zsh
yarn add global typescript // 글로벌
yarn add tsc-watch --dev // 개발용
```
&nbsp;
&nbsp;
### 2. 설정파일 작성

##### tsconfig.json 파일

```json
{
    "compilerOptions": {
        "module": "commonjs",
        "target": "es2015",
        "sourceMap": true,
        "outDir": "dist"
    },
    "include": [
        "src/**/*"
    ],
    "exclude": [
        "node_modules"
    ]
}
```
&nbsp;
&nbsp;
##### package.json 파일

```json
{
    "name": "typechain",
    "license": "MIT",
    "scripts": {
        "start": "tsc-watch --onSuccess \" node dist/index.js \"",
        "prestart": "tsc"
    },
    "devDependencies": {
        "tsc-watch": "^1.0.22"
    }
}
```
&nbsp;
&nbsp;
##### 폴더 구조 설정

![폴더구조](https://user-images.githubusercontent.com/36188268/42356431-666fc91a-810d-11e8-8c24-96953003a1bc.png)

![](https://user-images.githubusercontent.com/36188268/42356432-67ba1bb8-810d-11e8-8613-0f1c6f449ce0.png)
<br>
<br>
### 3. 테스트 코드

```js
console.log("Hello, Good!!!");

export {};
```
<br>
<br>