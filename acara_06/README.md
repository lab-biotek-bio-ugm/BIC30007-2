# NGS-Data-Processing-and-Variant-Calling

Alur kerja pemrosesan data NGS dan pemanggilan variasi sederhana. 

Menggunakan bwa, samtools, bcftools dan visualisasi dengan IGV.

# BIC30007-2 - Acara 6
See the main [README.md](../README.md) for general instructions.

## Using Google Colaboratory
### Upload the repository to Google Drive
The best way to run this course repository on google colab is via Google Drive.

If you haven't so:
- Find the latest release modul 6 from: https://github.com/lab-biotek-bio-ugm/BIC30007-2/releases
- Go to the `Assets` and download the source code `acara_06.zip`
- Unzip the source code in your local machine (laptop)
- Upload the whole directory to Google drive
- Open the notebook with google colab

### Installing dependencies
- On the first line, create a new cell and run:

```python
# install conda and mamba
!pip install -q condacolab
import condacolab
condacolab.install_mambaforge() # session will crash and restart
```
- Setelah session restart
```python
import condacolab
condacolab.check()

# mount drive
from google.colab import drive
drive.mount('/content/drive')
```
- Install dependencies
```python
# assume you have uploaded the repo to gdrive
!mamba env update -n base -f /content/drive/MyDrive/<your downloaded release name>/environment.yml
```
- Kemudian, masuk ke working directory
```python
# check and move your working directory into <your downloaded release name>
cd /content/drive/MyDrive/<your downloaded release name>
```

- Lanjut ke bagian pengaturan folder input, ganti `data_dir` sesuai path yang ada di colab. 
```python
# Set up paths
from pathlib import Path
data_dir = Path('/content/drive/MyDrive/<your downloaded release name>/data')
# Jika output dari data_dir.is_dir() adalah False, sesuaikan value dari data_dir dengan lokasi yang benar
assert data_dir.is_dir(), f"Folder {data_dir} tidak ditemukan, sesuaikan value dari data_dir dengan lokasi yang benar!"



```