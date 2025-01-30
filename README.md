# main.py

# List untuk menyimpan nama tamu
guest_list = []

def display_menu():
    print("\n==== Aplikasi Daftar Tamu ====")
    print("1. Tambahkan Nama Tamu")
    print("2. Lihat Daftar Tamu")
    print("3. Keluar")

def add_guest():
    guest_name = input("Masukkan nama tamu: ")
    guest_list.append(guest_name)
    print(f"{guest_name} berhasil ditambahkan ke daftar tamu!")

def view_guests():
    if guest_list:
        print("\nDaftar Tamu:")
        for index, guest in enumerate(guest_list, 1):
            print(f"{index}. {guest}")
    else:
        print("\nBelum ada tamu yang ditambahkan.")

def main():
    while True:
        display_menu()
        choice = input("Pilih menu: ")

        if choice == "1":
            add_guest()
        elif choice == "2":
            view_guests()
        elif choice == "3":
            print("Terima kasih telah menggunakan aplikasi ini!")
            break
        else:
            print("Pilihan tidak valid, coba lagi.")

if __name__ == "__main__":
    main()
