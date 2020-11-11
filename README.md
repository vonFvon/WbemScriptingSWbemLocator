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
>>string   CreationClassName; |
>>string   Caption; |
>>string   CommandLine; |
>>datetime CreationDate; |
>>string   CSCreationClassName; |
>>string   CSName; |
>>string   Description; |
>>string   ExecutablePath; |
>>uint16   ExecutionState; |
>>string   Handle; |
>>uint32   HandleCount; |
>>datetime InstallDate; |
>>uint64   KernelModeTime; |
>>uint32   MaximumWorkingSetSize; |
>>uint32   MinimumWorkingSetSize; |
>>string   Name; |
>>string   OSCreationClassName; |
>>string   OSName; |
>>uint64   OtherOperationCount; |
>>uint64   OtherTransferCount; |
>>uint32   PageFaults; |
>>uint32   PageFileUsage; |
>>uint32   ParentProcessId; |
>>uint32   PeakPageFileUsage; |
>>uint64   PeakVirtualSize; |
>>uint32   PeakWorkingSetSize; |
>>uint32   Priority = NULL; |
>>uint64   PrivatePageCount; |
>>uint32   ProcessId; |
>>uint32   QuotaNonPagedPoolUsage; |
>>uint32   QuotaPagedPoolUsage; |
>>uint32   QuotaPeakNonPagedPoolUsage; |
>>uint32   QuotaPeakPagedPoolUsage; |
>>uint64   ReadOperationCount; |
>>uint64   ReadTransferCount; |
>>uint32   SessionId; |
>>string   Status; |
>>datetime TerminationDate; |
>>uint32   ThreadCount; |
>>uint64   UserModeTime; |
>>uint64   VirtualSize; |
>>string   WindowsVersion; |
>>uint64   WorkingSetSize; |
>>uint64   WriteOperationCount; |
>>uint64   WriteTransferCount; |

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