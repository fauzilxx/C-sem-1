# C-sem-1
PROGRAM C YANG SAYA BUAT SELAMA 1 SEMESTER
#include <stdio.h>

int main() {
    char nama_barang[50];
    int jumlah_barang, harga_perunit;
    float harga_barang, harga_setelahdiskon;
    char ulangi;

    do {  
        // Input nama,jumlah, dan harga barang
        printf("MASUKKAN NAMA BARANG = ");
        scanf("%s", nama_barang);
        printf("MASUKKAN JUMLAH BARANG = ");
        scanf("%d", &jumlah_barang);
        printf("MASUKKAN HARGA PER UNIT = ");
        scanf("%d", &harga_perunit);

        // Hitung total harga
        harga_barang = harga_perunit * jumlah_barang;

        // Output data barang dan total harga
        printf("NAMA BARANG = %s\n", nama_barang);
        printf("JUMLAH BARANG = %d\n", jumlah_barang);
        printf("HARGA PER UNIT = %d\n", harga_perunit);
        printf("TOTAL HARGA = %.2f\n", harga_barang);

        // Cek apakah bisa mendapatkan diskon
        if (harga_barang > 100000) {
            harga_setelahdiskon = harga_barang * 0.9;  // Diskon 10%
            printf("HARGA SETELAH DISKON = %.2f\n", harga_setelahdiskon);
        } else {
            printf("HARGA TETAP, TIDAK MENDAPATKAN DISKON = %.2f\n",harga_barang);
        }

        // Tanyakan apakah ingin menginput barang lagi
        printf("APAKAH INGIN MENGINPUT LAGI (y/x?): ");
        scanf(" %c", &ulangi);  
    } while (ulangi == 'y' || ulangi == 'Y');

    return 0;
}
