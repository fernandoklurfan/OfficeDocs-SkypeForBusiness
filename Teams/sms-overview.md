

> [!NOTE]
> Whenever porting Direct Routing numbers to Teams using another PSTN connectivity option, the numbers must be released from Microsoft's telephone number management inventory. After unassigning the numbers from the users and before your number port event, use the PowerShell cmdlet [New-CsOnlineTelephoneNumberReleaseOrder](/powershell/module/teams/new-csonlinetelephonenumberreleaseorder) to make the Direct Routing numbers available for porting. A release order can also be used if you don't want to keep your acquired Direct Routing numbers in Microsoft's inventory.