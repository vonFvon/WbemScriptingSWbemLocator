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
>>uint16   AddressWidth;
>>uint16   Architecture;
>>string   AssetTag;
>>uint16   Availability;
>>string   Caption;
>>uint32   Characteristics;
>>uint32   ConfigManagerErrorCode;
>>boolean  ConfigManagerUserConfig;
>>uint16   CpuStatus;
>>string   CreationClassName;
>>uint32   CurrentClockSpeed;
>>uint16   CurrentVoltage;
>>uint16   DataWidth;
>>string   Description;
>>string   DeviceID;
>>boolean  ErrorCleared;
>>string   ErrorDescription;
>>uint32   ExtClock;
>>uint16   Family;
>>datetime InstallDate;
>>uint32   L2CacheSize;
>>uint32   L2CacheSpeed;
>>uint32   L3CacheSize;
>>uint32   L3CacheSpeed;
>>uint32   LastErrorCode;
>>uint16   Level;
>>uint16   LoadPercentage;
>>string   Manufacturer;
>>uint32   MaxClockSpeed;
>>string   Name;
>>uint32   NumberOfCores;
>>uint32   NumberOfEnabledCore;
>>uint32   NumberOfLogicalProcessors;
>>string   OtherFamilyDescription;
>>string   PartNumber;
>>string   PNPDeviceID;
>>uint16   PowerManagementCapabilities[];
>>boolean  PowerManagementSupported;
>>string   ProcessorId;
>>uint16   ProcessorType;
>>uint16   Revision;
>>string   Role;
>>boolean  SecondLevelAddressTranslationExtensions;
>>string   SerialNumber;
>>string   SocketDesignation;
>>string   Status;
>>uint16   StatusInfo;
>>string   Stepping;
>>string   SystemCreationClassName;
>>string   SystemName;
>>uint32   ThreadCount;
>>string   UniqueId;
>>uint16   UpgradeMethod;
>>string   Version;
>>boolean  VirtualizationFirmwareEnabled;
>>boolean  VMMonitorModeExtensions;
>>uint32   VoltageCaps;