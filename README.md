# What is moon
moon is a pasted cheat claiming to be uncrackable and undetect. (ITS PAID)
# Why i cracked it
Because they are selling a pasted & detect cheat, so scamming.

# THE DRIVER
<div align="center">
    <img src="https://cdn.discordapp.com/attachments/914987108387663953/914996533429174322/unknown.png"/>
</div>

(very undetect aswell)

# Their driver location if you wanna skid it
```cpp
 NTSTATUS __stdcall DriverEntry(PDRIVER_OBJECT DriverObject, PUNICODE_STRING RegistryPath)
{
  struct _UNICODE_STRING DestinationString; // [rsp+20h] [rbp-18h] BYREF

  sub_140001000(DriverObject, RegistryPath);
  sub_1400011B0();
  RtlInitUnicodeString(&DestinationString, L"\\Driver\\may2h2drve");
  IoCreateDriver(&DestinationString, sub_1400016F0);
  return 0;
}
```cpp
 RtlInitUnicodeString(&DestinationString, L"\\Device\\may2h2drve");
  result = IoCreateDevice(DriverObject, 0, &DestinationString, 0x22u, 0x100u, 0, &DeviceObject);
  if ( !result )
  {
    RtlInitUnicodeString(&SymbolicLinkName, L"\\DosDevices\\may2h2drve");
    result = IoCreateSymbolicLink(&SymbolicLinkName, &DestinationString);
}
```

# original driver
```cpp
   v23 = (char *)VirtualAddress + v21;
  if ( (char *)VirtualAddress + v21 )
  {
    LODWORD(v14) = *(_DWORD *)(v23 + 3) + 7;
    v24 = &v23[(int)v14];
    if ( v24 )
    {
      v25 = *((_QWORD *)v24 + 2);
      LODWORD(v14) = 5761729;
      v26 = *(_DWORD *)(v25 + 64);
      if ( v26 == 1473057813 || v26 == 1384442563 )
      {
        LODWORD(v30) = 1966108;
        *((_QWORD *)&v30 + 1) = L"may2h2drve.sys";
        *(_DWORD *)(v25 + 64) = 5761729;
        *(_OWORD *)(v25 + 48) = v30;
      }
      for ( j = *(__int64 **)(v25 + 32); j != *(__int64 **)(v25 + 40); LODWORD(v14) = (_DWORD)v14 + 1 )
      {
        v28 = *((_DWORD *)j + 8);
        if ( v28 == 1473057813 || v28 == 1384442563 )
        {
          LODWORD(v30) = 1966108;
          *((_QWORD *)&v30 + 1) = L"may2h2drve.sys";
          *((_DWORD *)j + 8) = (_DWORD)v14;
          *((_OWORD *)j + 1) = v30;
        }
        j = (__int64 *)*j;
      }
    }
  }
  return (char)v14;
}
}
```

# IOCTL...

```cpp
.idata:0000000140002038 ; __int64 __fastcall IoCreateDriver(_QWORD, _QWORD)
.idata:0000000140002038                 extrn IoCreateDriver:qword
```
as you can see they use ioctl...........


# THE MAPPER

Its kdmapper. And kdmapper mean detect.

<div align="center">
    <img src="https://cdn.discordapp.com/attachments/910143447569166398/914995630240325742/unknown.png"/>
</div>

LMAO.....
