# TugasPBO
# 1. Implementasikan kelas Mahasiswa, Jurusan dan Universitas sesuai dengan spesifikasi yang diberikan.
class Mahasiswa:
    def __init__(self, nama, nim, jurusan):
        self.Nama = nama
        self.NIM = nim
        self.Jurusan = jurusan
    
    def tampilkan_info(self):
        print("Nama    : ", self.Nama)
        print("NIM     : ", self.NIM)
        print("Jurusan : ", self.Jurusan.NamaJurusan)

class Jurusan:
    def __init__(self, nama_jurusan):
        self.NamaJurusan = nama_jurusan
        self.DaftarMahasiswa = []
    
    def tambah_mahasiswa(self, mahasiswa):
        self.DaftarMahasiswa.append(mahasiswa)
    
    def tampilkan_daftar_mahasiswa(self):
        for mahasiswa in self.DaftarMahasiswa:
            mahasiswa.tampilkan_info()
            print()

class Universitas:
    def __init__(self, nama_universitas):
        self.NamaUniversitas = nama_universitas
        self.DaftarJurusan = []
    
    def tambah_jurusan(self, jurusan):
        self.DaftarJurusan.append(jurusan)
    
    def tampilkan_daftar_jurusan(self):
        for jurusan in self.DaftarJurusan:
            print(jurusan.NamaJurusan)

# 2. Membuat objek Universitas XYZ.
universitas_xyz = Universitas("XYZ University")

# 3. Buatlah objek Jurusan dengan nama "Teknik Informatika" dan tambahkan objek tersebut ke dalam Universitas XYZ.
jurusan_ti = Jurusan("Teknik Informatika")
universitas_xyz.tambah_jurusan(jurusan_ti)

# 4. Buatlah objek Mahasiswa dengan nama "Kalian masing", NIM "Kalian masing", dan masukkan ke dalam Jurusan Teknik Informatika di Universitas XYZ.
mahasiswa_weko = Mahasiswa("Weko Abbror", "G1A022025", jurusan_ti)
jurusan_ti.tambah_mahasiswa(mahasiswa_weko)

# 5. Tampilkan daftar jurusan yang ada di Universitas XYZ.
print("Daftar Jurusan di XYZ University:")
universitas_xyz.tampilkan_daftar_jurusan()

# 6. Tampilkan daftar mahasiswa yang terdaftar dalam Jurusan Teknik Informatika di Universitas XYZ.
print("\nDaftar Mahasiswa di Jurusan Teknik Informatika:")
jurusan_ti.tampilkan_daftar_mahasiswa()
