# Data contoh: jari-jari atom untuk beberapa unsur (data fiktif)
atomic_numbers = np.arange(1, 11)  # Nomor atom 1 sampai 10
atomic_radii = np.array([0.5, 0.7, 0.9, 1.1, 1.3, 1.5, 1.7, 1.9, 2.1, 2.3])  # Jari-jari atom (satuan arbitrer)

# Fungsi untuk membuat satu frame animasi
def animate(i):
    plt.cla()
    plt.plot(atomic_numbers[:i+1], atomic_radii[:i+1], 'o-')
    plt.xlabel('Nomor Atom')
    plt.ylabel('Jari-jari Atom')
    plt.title('Perubahan Jari-jari Atom')

# Inisialisasi plot
fig, ax = plt.subplots()

# Buat animasi
ani = animation.FuncAnimation(fig, animate, frames=len(atomic_numbers), interval=500)

# Tampilkan animasi
plt.show()
