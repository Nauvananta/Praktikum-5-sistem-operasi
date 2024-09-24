# Praktikum-5-sistem-operasi

1. Eksekusi seluruh profile yang ada :                                                                                                        
a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :                                                
echo “Profile dari /etc/profile”                                                                                       
![Screenshot from 2024-09-24 19-17-14](https://github.com/user-attachments/assets/f89e9d09-ddc7-40f8-b232-0700f724c8f7)

b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :                                                 
/home/stD02001/.bash_profile                                                                                           
/home/. stD02001/.bash_login                                                                                           
/home/mahasiswa/.profile                                                                                              
/home/mahasiswa/.bashrc                                                                                                
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap                                                       
file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :                                
echo “Profile dari .bash_profile”                                                                                      
Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang                                     
bersangkutan.                                                                                                          
![Screenshot from 2024-09-24 19-33-26](https://github.com/user-attachments/assets/0ac8f0f6-c6a4-4c2f-809a-0ecd2772de33)
![Screenshot from 2024-09-24 19-32-49](https://github.com/user-attachments/assets/c3d3dba5-6e09-41e1-bec7-da56a6666f93)
![Screenshot from 2024-09-24 19-36-36](https://github.com/user-attachments/assets/2b418c23-75be-4463-9a8a-65d71a86f4b1)
![Screenshot from 2024-09-24 19-36-07](https://github.com/user-attachments/assets/c1798892-5ade-4a27-972c-2ae97e0ca524)
![Screenshot from 2024-09-24 19-37-34](https://github.com/user-attachments/assets/c413b0e7-2d26-4788-8c32-c23733af6ffd)
![Screenshot from 2024-09-24 19-38-45](https://github.com/user-attachments/assets/ef18155a-b37f-4a97-af9b-87170c4f32d8)

c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:                            
$ su mahasiswa                                                                                                         
$ exit                                                                                                                 
kemudian gunakan opsi – sebagai berikut :                                                                              
$ su – mahasiswa                                                                                                       
$ exit                                                                                                                 
Jelaskan perbedaan kedua utilitas tersebut.                                                                            
![Screenshot from 2024-09-24 19-41-03](https://github.com/user-attachments/assets/a34cc1cd-54bf-4793-943a-7cf2f918cc33)
Perintah su (substitute user) digunakan untuk berpindah pengguna dalam sistem Linux. Jika kita menjalankan su lblanket, kita hanya mengganti identitas pengguna ke lblanket tanpa mengubah lingkungan atau variabel dari pengguna sebelumnya, seperti PATH. Sedangkan, jika menggunakan su - lblanket, perintah ini tidak hanya mengganti pengguna tetapi juga memuat seluruh lingkungan pengguna lblanket, termasuk semua variabel dan pengaturan khususnya, sehingga sesi pengguna baru terasa seperti masuk dari awal. Kesimpulannya, perbedaan utama adalah pada lingkungan pengguna, di mana su - memuatnya secara penuh, sedangkan su tidak.

2. Prompt String (PS)                                                                                                    
a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan                            
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell                                 
PS1=‟> „                                                                                                               
export PS1                                                                                                             
b. Eksperimen hasil PS1 :                                                                                              
$ PS1=“\! > “                                                                                                          
69 > PS1=”\d > “                                                                                                       
Mon Sep 23 > PS1=”\t > “                                                                                               
10:10:20 > PS1=”Saya=\u > “                                                                                            
Saya=mahasiswa > PS1=”\w >”                                                                                            
~ > PS1=\h >”                                                                                                          
![Screenshot from 2024-09-24 19-45-23](https://github.com/user-attachments/assets/47806683-33c1-4e98-9d87-ed24f6ce5baa)
![Screenshot from 2024-09-24 19-42-24](https://github.com/user-attachments/assets/1e3c8969-532e-46ca-b6c0-26717323ee89)

3. Logout                                                                                                              
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout                              
Echo “Terima kasih atas sesi yang diberikan”                                                                           
Sleep 5                                                                                                                
clear
![Screenshot from 2024-09-24 19-53-04](https://github.com/user-attachments/assets/b8ce818b-f483-48b8-b0fa-30aaf5cc211e)
![Screenshot from 2024-09-24 19-51-37](https://github.com/user-attachments/assets/029aa920-c519-4ab9-b1ee-886f7f2a7607)

4. Bash script                                                                                                           
a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :                                                  
p1.sh                                                                                                                  
#! /bin/bash                                                                                                           
echo “Program p1”                                                                                                     
ls –l                                                                                                                  
p2.sh                                                                                                                  
#! /bin/bash                                                                                                           
echo “Program p2”                                                                                                      
who                                                                                                                    
p3.sh                                                                                                                  
#! /bin/bash                                                                                                           
echo “Program p3”                                                                                                      
ps x
![Screenshot from 2024-09-24 19-56-43](https://github.com/user-attachments/assets/430c5692-1534-4175-9991-f1115dceac41)
![Screenshot from 2024-09-24 19-54-41](https://github.com/user-attachments/assets/61b99d50-de84-413d-b1f2-9ca92bd7fe81)
![Screenshot from 2024-09-24 19-55-47](https://github.com/user-attachments/assets/371835e1-7da7-4b99-8983-fdda3cc5057b)
![Screenshot from 2024-09-24 19-56-32](https://github.com/user-attachments/assets/8d465d3b-9b7a-4d69-a3c4-d7ce0f1d63e2)

b. Jalankan script tersebut sebagai berikut :                                                                          
$ ./p1.sh ; ./p3.sh ; ./p2.sh                                                                                          
$ ./p1.sh &                                                                                                            
$ ./p1.sh $ ./p2.sh & ./p3.sh &                                                                                        
$ ( ./p1.sh ; ./p3.sh ) &                                                                                              
![Screenshot from 2024-09-24 20-15-12](https://github.com/user-attachments/assets/f4586291-ad70-47f6-ac25-7daf0f0d5eaf)
![Screenshot from 2024-09-24 20-15-53](https://github.com/user-attachments/assets/5edd0beb-3a6a-447c-b36d-dba204a21c86)
![Screenshot from 2024-09-24 20-20-17](https://github.com/user-attachments/assets/da55147c-ab77-4c5a-87d5-970de94da815)
![Screenshot from 2024-09-24 21-28-53](https://github.com/user-attachments/assets/e0bc6a8f-a8a8-4ab1-994b-1aa0a0b86f92)
