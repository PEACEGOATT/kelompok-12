# Menggunakan Python 3.9 sebagai base image
FROM python:3.9

# Menetapkan direktori kerja di dalam container
WORKDIR /app

# Menyalin file requirements.txt ke dalam container
COPY requirements.txt .

# Install dependencies dari requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Menyalin semua file proyek ke dalam container
COPY . .

# Menjalankan aplikasi Flask menggunakan Gunicorn
CMD ["gunicorn", "-b", "0.0.0.0:5000", "app:app"]
