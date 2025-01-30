def show_menu():
    print("==== Aplikasi Daftar Tamu ====")
    print("1. Tambahkan Nama Tamu")
    print("2. Lihat Daftar Tamu")
    print("3. Keluar")

def add_guest(guest_list):
    name = input("Masukkan nama tamu: ")
    guest_list.append(name)
    print(f"{name} telah ditambahkan!")

def view_guests(guest_list):
    if guest_list:
        print("Daftar Tamu:")
        for guest in guest_list:
            print(f"- {guest}")
    else:
        print("Belum ada tamu yang ditambahkan.")

def main():
    guest_list = []  # Inisialisasi list tamu
    while True:
        show_menu()  # Tampilkan menu
        choice = input("Pilih menu: ")  # Pilihan pengguna

        if choice == '1':
            add_guest(guest_list)  # Tambah tamu
        elif choice == '2':
            view_guests(guest_list)  # Lihat daftar tamu
        elif choice == '3':
            print("Terima kasih telah menggunakan aplikasi!")  # Keluar
            break
        else:
            print("Pilihan tidak valid, coba lagi.")

if __name__ == "__main__":
    main()
