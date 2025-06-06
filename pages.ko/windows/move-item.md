# Move-Item

> 파일, 디렉토리, 레지스트리 키 및 기타 PowerShell 데이터 항목을 이동 또는 이름을 변경합니다.
> 이 명령어는 PowerShell을 통해서만 실행할 수 있습니다.
> 더 많은 정보: <https://learn.microsoft.com/powershell/module/microsoft.powershell.management/move-item>.

- 목표가 기존 디렉토리가 아닐 때 파일 또는 디렉토리 이름 변경:

`Move-Item {{경로\대상\소스}} {{경로\대상\목표}}`

- 파일 또는 디렉토리를 기존 디렉토리로 이동:

`Move-Item {{경로\대상\소스}} {{경로\대상\기존_디렉토리}}`

- 특정 이름을 가진 파일 또는 디렉토리 이름 변경 또는 이동 (문자열 내 특수 문자 처리 안함):

`Move-Item -LiteralPath "{{경로\대상\소스}}" {{경로\대상\파일_또는_디렉토리}}`

- 여러 파일을 기존 디렉토리로 이동하고 파일 이름 변경 안함:

`Move-Item {{경로\대상\소스1 , 경로\대상\소스2 ...}} {{경로\대상\기존_디렉토리}}`

- 레지스트리 키 이동 또는 이름 변경:

`Move-Item {{경로\대상\소스_키1 , 경로\대상\소스_키2 ...}} {{경로\대상\새로운_또는_기존_키}}`

- 기존 파일 또는 레지스트리 키 덮어쓰기 전에 확인 안함:

`mv -Force {{경로\대상\소스}} {{경로\대상\목표}}`

- 파일 권한에 관계없이 기존 파일을 덮어쓰기 전에 확인 메시지를 표시:

`mv -Confirm {{경로\대상\소스}} {{경로\대상\목표}}`

- 건너뛰기 모드로 파일 이동, 이동할 파일 및 디렉토리 표시:

`mv -WhatIf {{경로\대상\소스}} {{경로\대상\목표}}`
