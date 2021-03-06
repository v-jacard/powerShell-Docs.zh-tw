# Just Enough Administration (JEA)
Just Enough Administration 是 WMF 5.0 中的新功能，可透過 PowerShell 遠端處理，啟用以角色為基礎的管理。  它會擴充現有受條件約束的端點基礎結構，方法是允許非系統管理員以系統管理員身分執行特定命令、指令碼和可執行檔。  這可讓您減少環境中具完整權限的系統管理員，並改善您的安全性。  JEA 適用於透過 PowerShell 所管理的所有項目；如果您可以運用 PowerShell 來管理某項目，則 JEA 可以協助您更安全地執行該動作。  如需深入了解 Just Enough Administration，請參閱[體驗指南](http://aka.ms/JEA)。

不同於舊的受條件約束之端點，JEA 功能強大且容易設定。  JEA 中的使用者功能可以更精細地控制，可精細到限制哪些參數集和值可提供給特定命令。 該使用者的動作可在一次性虛擬帳戶的情境下執行，其中該虛擬帳戶具有執行系統管理員動作的權限。  由該使用者叫用的命令可以針對安全性稽核記錄。

JEA 的運作方式是讓您能夠建立經過特別設定的受限制端點。  這些端點有幾項重要特性：

1. 連接到這些端點的使用者，其「執行身分」為具特殊權限的虛擬帳戶，存在期間僅限於此遠端工作階段。  根據預設，此虛擬帳戶是內建系統管理員群組的成員，也是網域控制站上的網域系統管理員 (請注意︰可設定這些權限)。 以一位使用者的身分連線，並以不同的特殊權限使用者身分執行，您可以允許非特殊權限的使用者執行特定的系統管理工作，而不需給予其您系統上的系統管理權限。
2. 端點已鎖定。  這表示 PowerShell 會在無語言模式中執行。  只有特定的命令、指令碼和可執行檔會顯示給使用者。
3. 不同的使用者連接會以一組根據群組成員資格的不同功能顯示。  您可以在相同的端點提供不同功能給不同角色。

<!--HONumber=Jun16_HO4-->


