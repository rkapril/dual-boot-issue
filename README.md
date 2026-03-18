# dual-boot (If you encounter issue booting to Ubuntu)

**After Ubuntu installed on partition Disk**

**Windows**

cmd run as adminstrator
```
bcdedit /set "{bootmgr}" path \EFI\ubuntu\grubx64.efi
```

grub>
```
ls
```

Look for `/boot/grub`

Set this with the correct disk 
```
set root=(hd0,gpt2)
set prefix=(hd0,gpt2)/boot/grub
insmod normal
normal
```
Once you in ubuntu
```
sudo grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=ubuntu
```
```
sudo update-grub
```

