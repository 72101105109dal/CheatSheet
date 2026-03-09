### Domain

PowerView.ps1

> Get-Domain <DomainName>
> 

> Get-Domain -Domain <DomainName>
> 

> Get-DomainController
> 

Powershell

> Get-ADDomain
> 

> Get-ADDomainController
> 

### User

PowerView.ps1

> Get-DomainUser
> 

> Get-DomainUser -Properties samaccountname
> 

<aside>

ADユーザーの中で、Descriptionに[built]が含まれるユーザー名のみ表示

</aside>

> Get-DomainUser -LDAPFilter "Description=*built*" | Select name
> 

<aside>

ローカルにログオンしたユーザー表示

</aside>

> Get-NetLoggedon
> 

> Get-LoggedOnLocal
> 

> Get-LastLoggedOn
> 

Powershell

> Get-ADUser
> 

> Get-ADUser -Filter ‘Description -like “*built*”’ - Properties Description | Select name,Description
> 

### Group

> Get-DomainGroup
> 

<aside>

ADグループ名の一覧表示

</aside>

> Get-DomainGroup　-Properties name
> 

<aside>

特定のADグループのメンバーを表示

</aside>

> Get-DomainGroup -LDAPFilter name=”<Group-Name>” | Select member
> 

> Get-DomainGroupMember "<Group-Name>" -Recurse
> 

<aside>

“admin”が含まれるADグループ名の一覧表示

</aside>

> Get-DomainGroup -LDAPFilter name=*admin* | Select name
> 

Powershell

> Get-ADGroup
> 

<aside>

ローカルのグループ

</aside>

> Get-NetLocalGroup
> 

> Get-NetLocalGroupMember
> 

### Computer

> Get-DomainComputer
> 

<aside>

dnshostname(=ADドメイン内のコンピューター名)は、<hostname>@domainの形式で表示する

</aside>

> Get-DomainComputer -Properties dnshostname
> 

### SID

PowerView.ps1

> Get-DomainSID
> 

### GPO

PowerView.ps1

<aside>

ドメインポリシーに関する情報取得

</aside>

> Get-DomainPolicyData
> 

CMD or Powershell

<aside>

適用中のGPOに関する情報取得

</aside>

> gpresult /r
> 

## GPO

<aside>

コマンドプロンプトかPowershellを管理者権限で実行

GPOの適用状況

</aside>

gpresult /r
