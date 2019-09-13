# learning_npm_talib

## Install talib

1. Use [windows-build-tools](https://www.npmjs.com/package/windows-build-tools)
2. Install `install --save talib`

## Usage

Use the already build-version in the `\talib` folder. 

## Errors

### Error: ENOENT: no such file or directory, scandir 'C:/Program Files (x86)/Reference Assemblies/Microsoft/Framework/.NETFramework'


1. Download talib from from github (https://github.com/oransel/node-talib)
2. Unpack it in the gekko directory and rename the unpacked directory to talib
3. Change the following line in talib\src\lib\build.js:
```
frameworkPath = 'C:/Program Files (x86)/Reference Assemblies/Microsoft/Framework/.NETFramework';
to
frameworkPath = 'C:/Program Files (x86)/Reference Assemblies/Microsoft/Framework';
```
3. Open cmd as administrator
4. Run: `npm install --vs2015 --global windows-build-tools` (be patient this may take a while [https://www.npmjs.com/package/windows-build-tools](https://www.npmjs.com/package/windows-build-tools)
5. Run: `install --save talib`

[Github Issue - Talib/Gekko](https://github.com/askmike/gekko/issues/1934)
