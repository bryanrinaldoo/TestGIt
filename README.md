# Sistem Operasi IF2230
> Tugas Besar MileStone 1 Kelompok ChaOS


## Table of contents
* [Cara Kerja Interrupt](#Cara_Kerja_Interrupt)
* [Cara Kerja kernel.asm](#Cara_Kerja_kernel.asm)
  * [_putInMemory](#_putInMemory)
  * [_interrupt](#_interrupt)
  * [_makeInterrupt21](#_makeInterrupt21)
  * [_handleInterrupt21](#_handleInterrupt21)
* [Author](#author)

## Cara Kerja Interrupt
Interrupt adalah sebuah proses pada komputer yang meminta untuk dilayani oleh prosesor. Interupsi terjadi bila suatu perangkat Input/output ingin memberitahu prosesor bahwa ia siap menerima perintah, output sudah dihasilkan,atau terjadi error.
Langkah kerja nya : 
1. Controller mengirimkan sinyal interupsi melalui interrupt-requestline, lalu Sinyal interupsi tersebut dideteksi oleh prosesor. 
2. Prosesor menyimpan informasi tentang keadaan state-nya. 
3. Prosesor mengidentifikasi penyebab interupsi dan menentukaninterrupt handler. 
4. Transfer kontrol ke interrupt handler.
5. Setelah teratasi, prosesor kembali ke keadaan semula. 

## Cara kerja kernel.asm 
Pada sistem operasi kami, terdapat sebuah kernel sederhana. Kernel ini berisikan 4 fungsi utama. 
Berikut adalah penjelan 4 fungsi utama tersebut : 

>### _putInMemory
void putInMemory (int segment, int address, char character)
Fungsi ini menulis sebuah karakter pada segment memori dengan offset tertentu


>### _interrupt
Fungsi ini memanggil sebuah interrupt dengan nomor tertentu dan juga meneruskan
parameter AX, BX, CX, DX berukuran 16-bit ke interrupt tersebut


>### _makeInterrupt21
Fungsi ini mempersiapkan tabel interrupt vector untuk memanggil kode Anda jika
interrupt 0x21 terpanggil



>### _handleInterrupt21
Fungsi ini dipanggil saat terjadi interrupt nomor 0x21. Implementasi interrupt 0x21 pada
kernel dilakukan di sini


## Author
* 13519057 Kadek Dwi Bagus Ananta Udayana
* 13519065 Faris Aziz
* 13519103 Bryan Rinaldo
