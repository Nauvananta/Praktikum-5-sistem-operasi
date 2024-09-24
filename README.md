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
![Screenshot from 2024-09-24 19-45-23](https://github.com/user-attachments/assets/47806683-33c1-4e98-9d87-ed24f6ce5baa)
![Screenshot from 2024-09-24 19-42-24](https://github.com/user-attachments/assets/1e3c8969-532e-46ca-b6c0-26717323ee89)

b. Eksperimen hasil PS1 :
$ PS1=“\! > “
69 > PS1=”\d > “
Mon Sep 23 > PS1=”\t > “
10:10:20 > PS1=”Saya=\u > “
Saya=mahasiswa > PS1=”\w >”
~ > PS1=\h >”

