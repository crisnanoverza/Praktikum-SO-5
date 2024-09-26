# Praktikum-SO-5
# NAMA : Crisna Noverza
# NIM : 09011182328002
# Mata Kuliah : SISTEM OPERASI
# Tugas-Praktikum-5-job-control
<h2>1. Eksekusi seluruh profile yang ada :  
a.  Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : </h2> <br/>
echo “Profile dari /etc/profile”  <br/>
<img src = https://github.com/user-attachments/assets/5daecb54-bb69-4a62-b393-25570d33684b width=500/> <br/>
<h2>b.  Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :</h2>  <br/>
/home/stD02001/.bash_profile  <br/>
/home/. stD02001/.bash_login  <br/>
/home/mahasiswa/.profile  <br/>
/home/mahasiswa/.bashrc  <br/>
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap  
file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :  <br/>
echo “Profile dari .bash_profile”  <br/>
<h2>Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang 
bersangkutan. </h2><br/>
<img src = https://github.com/user-attachments/assets/cebfd902-61ed-4366-9127-35e90edc7ca2 width=500/><br/>
<h2>c.  Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:  </h2><br/>
$ su mahasiswa  <br/>
$ exit <br/>
<img src = https://github.com/user-attachments/assets/118ba3a7-3b05-4977-b2f1-8b8d429e4901 width=500/><br/>
<h2>kemudian gunakan opsi – sebagai berikut : </h2> <br/>
$ su – mahasiswa  <br/>
$ exit  <br/>
<img src = https://github.com/user-attachments/assets/fc0ebc4a-8cbe-451b-b78d-bcef9a563adf width=500/><br/>

<h2>Jelaskan perbedaan kedua utilitas tersebut.  </h2><br/>
<h2>1. su mahasiswa:</h2>
<P>Perintah ini menjalankan su untuk beralih ke user mahasiswa.
Saat menggunakan perintah ini tanpa opsi -, lingkungan (environment) dari user saat ini tetap dipertahankan. Artinya, hanya identitas pengguna yang berubah, tetapi variabel lingkungan seperti PATH tidak akan berubah.</P>
Jadi, variabel lingkungan dan direktori kerja yang sedang aktif tetap sama seperti sebelumnya.<br/>

<h2>2. su - mahasiswa:</h2>
<p>Perintah ini menggunakan opsi - yang dikenal sebagai login shell.
Opsi ini melakukan login penuh sebagai user mahasiswa, sehingga environment yang dimuat adalah environment milik mahasiswa secara lengkap. Ini termasuk mengubah direktori kerja ke home directory user mahasiswa dan memuat variabel lingkungan seperti yang didefinisikan dalam shell milik mahasiswa.</p>
Jadi, ini seperti memulai sesi baru sebagai user mahasiswa.<br/>

<h2>2. Prompt String (PS)  
a.    Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan 
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell </h2> <br/>
PS1=‟> „  <br/>
export PS1  <br/>
<img src = https://github.com/user-attachments/assets/340498c4-9da7-4c0b-b8cd-793e92582fd5 width=500/><br/>
<h2>b.  Eksperimen hasil PS1 :  </h2><br/>
$ PS1=“\! > “  <br/>
69 > PS1=”\d > “  <br/>
Mon Sep 23 > PS1=”\t > “<br/>  
10:10:20 > PS1=”Saya=\u > “  <br/>
Saya=mahasiswa > PS1=”\w >”  <br/>
~ > PS1=\h >” <br/>
<img src = https://github.com/user-attachments/assets/f6904b33-f80f-4fb3-a4ba-089ced948ffc width=500/><br/>
<img src = https://github.com/user-attachments/assets/82c206d1-8b10-470e-995f-5615eaf787a2 width=500/><br/>
<h2>3. Logout  
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout  </h2>
Echo “Terima kasih atas sesi yang diberikan”  <br/>
Sleep 5  <br/>
clear <br/>
<img src = https://github.com/user-attachments/assets/0bbc247c-5c73-4f85-8570-d5d261521e57 width=500/><br/>
<img src = https://github.com/user-attachments/assets/a579f8a0-a6ae-45ac-80f8-49228e8cdaef width=500/><br/>
<h2>4. Bash script  <br/>
a.  Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :  </h2><br/>
p1.sh  <br/>
#! /bin/bash  <br/>
echo “Program p1”  <br/>
ls –l  <br/>
p2.sh  <br/>
#! /bin/bash  <br/>
echo “Program p2”  <br/>
who  <br/>
p3.sh  <br/>
#! /bin/bash<br/>  
echo “Program p3”<br/>  
ps x  <br/>
<img src = https://github.com/user-attachments/assets/faa6ebb2-adef-42b3-b7b7-5992c491fac8 width=500/> <br/>
<img src = https://github.com/user-attachments/assets/1332e156-4ea0-47c6-838e-4c3ad441ae38 width=500/> <br/>
<img src = https://github.com/user-attachments/assets/2fe9b4de-746a-40e1-99f7-f4c054255477 width=500/><br/>
<img src = https://github.com/user-attachments/assets/7d2875d8-40f5-4e84-8eba-a6919b84712b width=500/><br/>
<h2>b.  Jalankan script tersebut sebagai berikut :  </h2>
$  ./p1.sh ; ./p3.sh ; ./p2.sh  <br/>
<img src = https://github.com/user-attachments/assets/4d9f753f-111e-4644-8e6a-dad51a28754d width=500/><br/>
<img src = https://github.com/user-attachments/assets/c3c7980f-4faf-4e41-8e20-57bc50c669b4 width=500/><br/>
<img src = https://github.com/user-attachments/assets/1361a33a-e58f-4ff1-843b-da834168edb7 width=500/><br/>
$  ./p1.sh &  <br/>
<img src = https://github.com/user-attachments/assets/bb9ebe5e-0db8-4be4-9d0b-83d0093e2f1c width=500/><br/>
$  ./p1.sh $ ./p2.sh & ./p3.sh & <br/> 
<img src = https://github.com/user-attachments/assets/efe786e8-50e5-4b4c-8345-1f46f7d184a4 width=500/><br/>
<img src = https://github.com/user-attachments/assets/58d9b470-f967-4854-80d1-c15e516fdda9 width=500/><br/>
<img src = https://github.com/user-attachments/assets/1cd97ddf-c031-4296-a02d-8bbc16358284 width=500/><br/>
$  ( ./p1.sh ; ./p3.sh ) & <br/>
<img src = https://github.com/user-attachments/assets/f0ac1aae-84de-4d4d-accc-15bbc0a8f046 width=500/><br/>
<img src = https://github.com/user-attachments/assets/e6ef3de2-2865-4e0c-9037-598d3539cb52 width=500/><br/>
<h2>5. Jobs  <br/>
a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh,  <br/>
setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.  </h2><br/>
#!/bin/bash  <br/>
while [ true ]  <br/>
do  <br/>
date >> hasil<br/>  
sleep 10  <br/>
done <br/>
<img src = https://github.com/user-attachments/assets/7bf6991f-c7e6-4c1e-a9cf-177083862dbf width=500/>/>
<h2>b.  Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background 
sebagai berikut : </h2> <br/>
$ jobs  <br/>
$ find / -print > files 2>/dev/null &  <br/>
$ jobs  <br/>
<img src = https://github.com/user-attachments/assets/f16d9e11-bd68-4a59-935d-9cc92f47d8eb width=500/><br/>
<h2>c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke 
background  </h2><br/>
$ fg %1  <br/>
$ bg <br/>
<img src = https://github.com/user-attachments/assets/a6e93142-bdb9-4989-bc26-584433695f70 width=500/><br/>
<h2>d.  Stop program background dengan utilitas kil  </h2><br/>
$ ps x  <br/>
<img src = https://github.com/user-attachments/assets/446d5e38-6cd0-4b28-9cf2-56d109bec81c width=500/><br/>
$ kill [Nomor PID] <br/>
<img src = https://github.com/user-attachments/assets/0c2067eb-57a3-41eb-a4ee-2a87bea7dda8 width=500/><br/>
<img src = https://github.com/user-attachments/assets/2a1ed038-bb93-45dc-b5f1-23d759e556ef width=500/><br/>
<h2>6. History  <br/>
a. Ganti nilai HISTSIZE dari 1000 menjadi 20  </h2><br/>
$ HISTSIZE=20  <br/>
$ history<br/>
<img src = https://github.com/user-attachments/assets/527f8226-5676-47a2-8a2e-337772e6fef8 width=500/><br/>
<h2>b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir 
dilakukan  </h2><br/>
$ !-5 <br/>
<img src = https://github.com/user-attachments/assets/c832a1cc-e558-44a7-b476-379814da5e25 width=500/><br/>
<h2>c. Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer  </h2><br/>
$ !!  <br/>
<img src = https://github.com/user-attachments/assets/52ff41ef-7226-4385-9fa6-c0a27487ada1 width=500/><br/>
<h2>d.  Ulangi instruksi pada history bufer nomor 150  </h2><br/>
$ !150  <br/>
<img src = https://github.com/user-attachments/assets/32031622-f1f5-469f-a3d8-88aaa7211b39 width=500/><br/>
<h2>e.  Ulangi instruksi dengan prefix “ls”  </h2>
$ !ls  <br/>
<img src = https://github.com/user-attachments/assets/f5926036-bdda-40c6-b584-5a60c59e7da0 width=500/><br/>
