import requests
import time

def send_message(url, message, count, interval):
    success_count = 0
    for i in range(count):
        data = {'message': message}
        response = requests.post(url, data=data)

        if response.status_code == 200:
            success_count += 1
            print(f'Pesan {i+1} berhasil dikirim!')
        else:
            print(f'Gagal mengirim pesan {i+1}:', response.status_code)

        if i < count - 1:
            time.sleep(interval)
    
    print(f'\nJumlah pesan yang berhasil dikirim: {success_count} dari {count}')

def main():
    print("SCRIPT BY ReeMods v1.0")
    print("\n(Menu)")
    
    url = input('Masukkan URL NGL yang dituju: ')
    message = input('Masukkan isi pesan Anda: ')
    count = int(input('Masukkan jumlah pesan yang dikirim: '))
    interval = float(input('Masukkan interval waktu antar pengiriman pesan (dalam detik): '))
    
    send_message(url, message, count, interval)

if __name__ == '__main__':
    main()
