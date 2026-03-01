# CSGI Specification: Canonical Skeleton Graph Interface

**Status**: Normative / Mandatory for cross-engine reproducibility.

## 1. Definition
**CSGI (Canonical Skeleton Graph Interface)** adalah antarmuka formal ("pengunci implementasi") yang menetapkan aturan untuk mengubah **Rasm Kanonik** (badan huruf Hijaiyyah tanpa nuqṭah) menjadi graf skeleton tertanam **Γ(h)** yang dapat direproduksi secara bit-identik di berbagai platform.

## 2. Output Contract
CSGI tidak memaksa implementor menggunakan satu algoritma skeletonisasi tertentu (misal: Zhang-Suen vs. Guo-Hall). Namun, CSGI mengunci **kontrak keluaran (Output Contract)** yang meliputi:
- **Nodes**: Koordinat titik cabang (junctions) dan titik terminasi.
- **Edges**: Polylines yang menghubungkan node, direpresentasikan sebagai urutan koordinat piksel/subpiksel.
- **Embedding**: Penempatan graf dalam koordinat Cartesian yang didefinisikan.
- **Metadata**: Informasi tambahan seperti derajat node dan arah edge.

## 3. Auditing & Reproducibility
Dengan mengunci kontrak keluaran, CSGI memastikan bahwa:
1. Pemetaan ke **MainPath** (jalur utama karakter) bersifat deterministik.
2. Perhitungan **Turning Codex** (perubahan sudut/kurvatur) dapat diaudit secara forensik.
3. Hasil audit pada Level Graf konsisten lintas mesin (Windows/Linux/Hardware).

## 4. Requirement
Implementasi atau auditor yang menginginkan status **Release-Grade Reproducibility** pada level graf wajib mengikuti skema CSGI yang telah ditetapkan dalam `CSGI-28-v1.0.json`.
