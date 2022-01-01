## Пропатченный чекер из intra для push_swap.
В чекере для **push_swap** была найдена скратя возможность визуализировать сортировку. После патча, эта функция стала доступна:
![patched_cheker](https://user-images.githubusercontent.com/83474704/147847400-34957502-375d-42a3-ba8f-6cf27e8e29d3.JPG)


В версии для **mac os** был пропатчен **cmp** (`66 39 C0`): `cmp dword ptr [rax+58h], 1` -> `cmp ax, ax`  
Был затерт лишний байт (`90`): `nop`
![mac_os](https://user-images.githubusercontent.com/83474704/147847114-992542e2-47e5-4f90-876a-7909e7d1bb21.JPG)


В версии для **linux** был пропатчен **cmp** (`39 C0`): `cmp eax, 0` -> `cmp eax, eax`  
Был затерт лишний байт (`90`): `nop`
![linux](https://user-images.githubusercontent.com/83474704/147847352-d2fbe156-4bf6-4b7a-b8aa-a2679b2b7142.png)
