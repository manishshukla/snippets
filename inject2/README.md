Inject2
--
 Files:<br/>
+ main.cpp
+ main.h
+ payload.h
<br/>
<hr/>
What it does:<br/>
1) Creates a new suspended process of calc.exe - using CreateProcessInternalW<br/>
2) Adds a new section and copy payload there<br/>
3) Creates a new suspended thread that will run the payload<br/>
4) Resumes threads (main of calc.exe and the newly created one)<br/>
<hr/>
Used functions:<br/>
+ kernel32.CreateProcessInternalW
+ ntdll.ZwCreateSection
+ ntdll.NtMapViewOfSection
+ ntdll.memcpy
+ ntdll.NtMapViewOfSection
+ ntdll.ZwUnmapViewOfSection
+ ntdll.ZwClose
+ ntdll.NtCreateThreadEx
