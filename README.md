def hitung_ips():
  """
  Fungsi untuk menghitung Indeks Prestasi Semester (IPS).
  """

  jumlah_matkul = int(input("Masukkan jumlah mata kuliah: "))
  total_bobot = 0
  total_sks = 0

  for i in range(jumlah_matkul):
    nilai = input(f"Masukkan nilai mata kuliah ke-{i+1} (A/B/C/D): ").upper()
    sks = 3  # Diasumsikan SKS setiap mata kuliah selalu 3

    if nilai == 'A':
      bobot = 4
    elif nilai == 'B':
      bobot = 3
    elif nilai == 'C':
      bobot = 2
    elif nilai == 'D':
      bobot = 1
    else:
      print("Nilai tidak valid!")
      return

    total_bobot += bobot * sks
    total_sks += sks

  ips = total_bobot / total_sks
  print(f"IPS: {ips:.2f}")

# Bagian utama program
hitung_ips()
