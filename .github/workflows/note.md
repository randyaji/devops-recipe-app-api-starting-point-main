# Simpan semua perubahan di branch prod
git stash push -u -m "Changes for staging"

# Pindah ke main
git switch main

# Update main dari GitHub
git pull origin main

# Terapkan kembali perubahan tadi
git stash pop

# Tambahkan semua perubahan secara otomatis
git add -A

# Commit
git commit -m "Update infrastructure configuration"

# Push ke staging
git push origin main
Setelah staging berhasil dan sudah dites:

Buat Pull Request di GitHub dari main ke prod.

Review perubahan, lalu merge.

Workflow akan berjalan lagi di branch prod untuk deployment production.
