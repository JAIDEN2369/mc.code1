
{ Game: Minecraft.Windows.exe
Version : 1.18 
Date: 2022
Author : JAIDEN1940

This script does  fly.c 
}

#pragma  once
#include <windows.h>
#include <tlhelp32.h>
#include <iostream>

extern DWORD baseAddress;
extern DWORD engineAddress;
extern DWORD clientState;


extern HANDLE hProcSnap;
extern PROCESSENTRY32 procEntry32;

extern HANDLE hModuleSnap;
extern MODULEENTRY32 modEntry32;

extern DWORD pID;

extern HANDLE hProc;


template <class dataType>
void wpm(dataType valToWrite, DWORD addressToWrite)
{
	WriteProcessMemory(hProc, (PVOID)addressToWrite, &valToWrite, sizeof(dataType), 0);
}


template <class dataType>
dataType rpm(DWORD addressToRead)
{

	dataType rpmBuffer;


	ReadProcessMemory(hProc, (PVOID)addressToRead, &rpmBuffer, sizeof(dataType), 0);


	return rpmBuffer;
}
 
int main()
{
	DWORD memoryAdress = 0xE7D982

		attachproc((char)minecraft.window.exe);

	while(true)
	{
		wpm [rax + 08], 2
			jne code
			mov eax, 1
			ret


		movzx eax, byte ptr[rax + 04]
			ret
			jmp return

	}
}
