# Unit for exception logging in Delphi applications

To use it, follow the instructions in the code comments.</br>
The logs created contain the stack trace and line number where the exception occured. </br>
Here is a log file example:

<pre>
EIBNativeException: [FireDAC][Phys][FB]violation of PRIMARY or UNIQUE KEY constraint "CORR_KEY" on table "CDR"
Problematic key value is ("IMAGEFILEPREFIX" = '_090aa791a77338aa7aass987_')
At procedure 'INSERT_IN_CDR' line: 182, col: 3
----------------------------
[000000000060AC41] JclDebug.TJclStackInfoList.Create + $151
[000000000060A788] JclDebug.JclCreateStackList + $48
[000000000060A696] JclDebug.DoExceptionStackTrace + $76
[000000000060C0E2] JclDebug.DoExceptNotify + $92
[00000000005FD8B5] JclHookExcept.TNotifierItem.DoNotify + $35
[00000000005FDAFB] JclHookExcept.DoExceptNotify + $BB
[00000000005FDC55] JclHookExcept.HookedRaiseException + $75
[00000000004122D3] System.@RaiseAtExcept + $103
[0000000000412338] System.@RaiseAgain + $38
[000000000105F244] FireDAC.Comp.Client.TFDCustomCommand.InternalExecute + $224
[000000000105F64F] FireDAC.Comp.Client.TFDCustomCommand.Execute + $3F
[0000000001068CD5] FireDAC.Comp.Client.TFDAdaptedDataSet.DoExecuteSource + $45
[00000000010148D1] FireDAC.Comp.DataSet.TFDDataSet.Execute + $B1
[000000000106C8F9] FireDAC.Comp.Client.TFDCustomStoredProc.ExecProc + $19
<b>[000000000113BB1C] faxjob.TFaxJob.InsertFaxInCDRDB (Line 574, "faxjob.pas" + 19) + $0</b>
[00000000011458C3] infthread.TInThread.ProcessIncomming (Line 267, "infthread.pas" + 83) + $10
[0000000001144C56] infthread.TInThread.Execute (Line 135, "infthread.pas" + 7) + $0
[000000000054F7A3] System.Classes.ThreadProc + $43
[0000000000412EAD] System.ThreadWrapper + $3D
[00007FF8C5767034] BaseThreadInitThunk + $14
[00007FF8C5A62651] RtlUserThreadStart + $21
</pre>
