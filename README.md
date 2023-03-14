# BIC30007-2 - Acara 2
See the main [README.md](../README.md) for general instructions.

## Using Google Colaboratory
### Upload the repository to Google Drive
The best way to run this course repository on google colab is via Google Drive.

If you haven't so:
- Find the latest release from: https://github.com/lab-biotek-bio-ugm/BIC30007-2/releases
- Go to the `Assets` and download the source code (either `zip` or `tar.gz`)
- Unzip (or untar) the source code in your local machine (laptop)
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
!mamba env update -n base -f /content/drive/MyDrive/<your downloaded release name>/acara_02/environment.yml
```
- Import Bio and Path
```python
# Import Bio
import Bio
from Bio import SeqIO

# Import Path
from pathlib import Path
```

- Lanjut ke bagian pengaturan folder input dan output, ganti `data_dir` sesuai path yang ada di colab. Contoh untuk notebook 02.1:
```python
# Set up paths
data_dir = Path('/content/drive/MyDrive/<your downloaded release name>/acara_02/data')
# Jika output dari data_dir.is_dir() adalah False, sesuaikan value dari data_dir dengan lokasi yang benar
assert data_dir.is_dir(), f"Folder {data_dir} tidak ditemukan, sesuaikan value dari data_dir dengan lokasi yang benar!"

# Set up output directory
output_dir = Path('/content/drive/MyDrive/<your downloaded release name>/acara_02/results/02.1')
output_dir.mkdir(parents=True, exist_ok=True)

# contoh penggunaan pathlib
contoh_path = data_dir / "1st_BASE_3766078_S1_F.ab1" # menambahkan child dir atau file dengan notasi "/"
print(contoh_path, contoh_path.is_file()) # Melakukan pengecekan apakah path yang diberikan berupa file atau bukan
```