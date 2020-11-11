### WbemScriptingSWbemLocator
#### What is ActiveX control?
ActiveX controls are small apps that allow websites to provide content such as videos and games when you browse the web. Occasionally, these apps can work incorrectly. In some cases, hese apps might be used to collect info from your PC. 

#### ActiveXObject Annotation (WbemScripting.SWbemLocator)
You can use the methods of the SWbemLocator object to obtain an SWbemServices object. The ConnectServer method of the SWbemLocator object connects to the namespace on either local or remote host computer equipped with WMI. This object can be created by the JavaScript ActiveXObject call.
   
    var locator = new ActiveXObject("WbemScripting.SWbemLocator");
	var service = locator.ConnectServer(".");
   
Now,  you connect to WMI on the specified computer.
   
    var properties = service.ExecQuery("SELECT * FROM Win32_Process");
	var np = new Enumerator(properties);
   
Finally, you need the ExecQuery method of the SWbemServices object in order to execute a query to retrieve objects. These objects are available through the returned SWbemObjectSet collection.

By the way, you must browse the sample on Internet Explorer and allow blocked content.

#### Remarks
###### Win32_Process WMI class represents a process on an operating system.
- Properties :
>> string   CreationClassName;<br/>
>> string   Caption;<br/>
>> string   CommandLine;<br/>
>> datetime CreationDate;<br/>
>>string   CSCreationClassName;<br/>
>>string   CSName;<br/>
>>string   Description;<br/>
>>string   ExecutablePath;<br/>
>>uint16   ExecutionState;<br/>
>>string   Handle;<br/>
>>uint32   HandleCount;<br/>
>>datetime InstallDate;<br/>
>>uint64   KernelModeTime;<br/>
>>uint32   MaximumWorkingSetSize;<br/>
>>uint32   MinimumWorkingSetSize;<br/>
>>string   Name;<br/>
>>string   OSCreationClassName;<br/>
>>string   OSName;<br/>
>>uint64   OtherOperationCount;<br/>
>>uint64   OtherTransferCount;<br/>
>>uint32   PageFaults;<br/>
>>uint32   PageFileUsage;<br/>
>>uint32   ParentProcessId;<br/>
>>uint32   PeakPageFileUsage;<br/>
>>uint64   PeakVirtualSize;<br/>
>>uint32   PeakWorkingSetSize;<br/>
>>uint32   Priority = NULL;<br/>
>>uint64   PrivatePageCount;<br/>
>>uint32   ProcessId;<br/>
>>uint32   QuotaNonPagedPoolUsage;<br/>
>>uint32   QuotaPagedPoolUsage;<br/>
>>uint32   QuotaPeakNonPagedPoolUsage;<br/>
>>uint32   QuotaPeakPagedPoolUsage;<br/>
>>uint64   ReadOperationCount;<br/>
>>uint64   ReadTransferCount;<br/>
>>uint32   SessionId;<br/>
>>string   Status;<br/>
>>datetime TerminationDate;<br/>
>>uint32   ThreadCount;<br/>
>>uint64   UserModeTime;<br/>
>>uint64   VirtualSize;<br/>
>>string   WindowsVersion;<br/>
>>uint64   WorkingSetSize;<br/>
>>uint64   WriteOperationCount;<br/>
>>uint64   WriteTransferCount;<br/>

###### Win32_Processor WMI class represents a device that can interpret a sequence of instructions on a computer running on a Windows operating system.
- Properties :
>>uint16   AddressWidth;<br/>
>>uint16   Architecture;<br/>
>>string   AssetTag;<br/>
>>uint16   Availability;<br/>
>>string   Caption;<br/>
>>uint32   Characteristics;<br/>
>>uint32   ConfigManagerErrorCode;<br/>
>>boolean  ConfigManagerUserConfig;<br/>
>>uint16   CpuStatus;<br/>
>>string   CreationClassName;<br/>
>>uint32   CurrentClockSpeed;<br/>
>>uint16   CurrentVoltage;<br/>
>>uint16   DataWidth;<br/>
>>string   Description;<br/>
>>string   DeviceID;<br/>
>>boolean  ErrorCleared;<br/>
>>string   ErrorDescription;<br/>
>>uint32   ExtClock;<br/>
>>uint16   Family;<br/>
>>datetime InstallDate;<br/>
>>uint32   L2CacheSize;<br/>
>>uint32   L2CacheSpeed;<br/>
>>uint32   L3CacheSize;<br/>
>>uint32   L3CacheSpeed;<br/>
>>uint32   LastErrorCode;<br/>
>>uint16   Level;<br/>
>>uint16   LoadPercentage;<br/>
>>string   Manufacturer;<br/>
>>uint32   MaxClockSpeed;<br/>
>>string   Name;<br/>
>>uint32   NumberOfCores;<br/>
>>uint32   NumberOfEnabledCore;<br/>
>>uint32   NumberOfLogicalProcessors;<br/>
>>string   OtherFamilyDescription;<br/>
>>string   PartNumber;<br/>
>>string   PNPDeviceID;<br/>
>>uint16   PowerManagementCapabilities[];<br/>
>>boolean  PowerManagementSupported;<br/>
>>string   ProcessorId;<br/>
>>uint16   ProcessorType;<br/>
>>uint16   Revision;<br/>
>>string   Role;<br/>
>>boolean  SecondLevelAddressTranslationExtensions;<br/>
>>string   SerialNumber;<br/>
>>string   SocketDesignation;<br/>
>>string   Status;<br/>
>>uint16   StatusInfo;<br/>
>>string   Stepping;<br/>
>>string   SystemCreationClassName;<br/>
>>string   SystemName;<br/>
>>uint32   ThreadCount;<br/>
>>string   UniqueId;<br/>
>>uint16   UpgradeMethod;<br/>
>>string   Version;<br/>
>>boolean  VirtualizationFirmwareEnabled;<br/>
>>boolean  VMMonitorModeExtensions;<br/>
>>uint32   VoltageCaps;<br/>