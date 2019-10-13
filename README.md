# Resource-Announcement-Project Angola-27
# This is all being done in the Resource Announcement directory in the /scratch_30_day_tmp/wadion pathway
1. Download Angola 27 Read 1: gdown.pl https://drive.google.com/file/d/1cj-Trrc62XB5SgfRNQkj0QgDKwIx8ViC/edit Ang27_R1.fastq.gz
2. Download Angola 27 Read 2: gdown.pl https://drive.google.com/file/d/14CNdXmNe6umynWgBkFPiGmBT-LY6jept/edit Ang27_R2.fastq.gz
3. Read 1 QA/QC: fastqc Ang27_R1.fastq.gz
4. Read 2 QA/QC: fastqc Ang27_R2.fastq.gz
5. Use WinSCP to move the QA/QC files to the Resource Announcement file on my H: drive
6. R1 QA/QC: file:///H:/BL5300/Resource%20Announcement/Ang27_R1_fastqc.html - Failures for "Per tile sequence quality" and "Per base sequence content" - Warnings for "Per base sequence quality", "Per sequence GC content", "Sequence Length Distribution", and "Overrepresented sequences"
7. R2 QA/QC: file:///H:/BL5300/Resource%20Announcement/Ang27_R2_fastqc.html - Failures for "Per base sequence quality", "Per tile sequence quality", "Per base sequence content", and "Per base N content" - Warnings for "Sequence Length Distribution" and "Overrepresented sequences"
8. Use cutadapt for read 1(R1) and read 2(R2)
9. QA/QC using cutadapt: cutadapt -q 20,20 -a CTGTCTCTTATACACATCTCCGAGCCCACGAGAC -A CTGTCTCTTATACACATCTGACGCTGCCGACGA -m 50 --max-n 0 -o Ang27_R1.cutadapt.fastq -p Ang27_R2.cutadapt.fastq Ang27_R1.fastq.gz Ang27_R2.fastq.gz
10. Post-cutadapt Read 1 QA/QC: fastqc Ang27_R1.cutadapt.fastq
11. Post-cutadapt Read 2 QA/QC: fastqc Ang27_R2.cutadapt.fastq
12. Use WinSCP to move the post-cutadapt QA/QC files to the Resource Announcement file on my H: drive
13. Post-cutadapt R1 QA/QC: file:///H:/BL5300/Resource%20Announcement/Ang27_R1.cutadapt_fastqc.html - Failures for "Per tile sequence quality" and "Per base sequence content" - Warnings for "Sequence Length Distribution
14. Post-cutadapt R2 QA/QC: file:///H:/BL5300/Resource%20Announcement/Ang27_R2.cutadapt_fastqc.html - Failures for "Per base sequence quality", "Per tile sequence quality and "Per base sequence content" - Warnings for "Sequence Length Distribution
15.
