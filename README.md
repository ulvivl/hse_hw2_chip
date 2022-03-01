# hse_hw2_chip

[Ссылка на колаб](https://colab.research.google.com/drive/1cnSsux6vQHfxGYYd3DwXDIJ9jJ8b69io?usp=sharing)<br>
[Ссылка на условия](https://docs.google.com/document/d/1bPVShA20DJureQI5SPLIb8_Ls3vTnrX46WunIZkpgFk/edit)

---
Клеточная линия | Гистоновая метка | Реплика 1 | Реплика 2 | Контрольный эксперимент 
--- | --- | --- | --- | ---
A549 | H3K4me2 | ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ

---
1. При анализе Fastqc подрезание прочтений и фильтрация не потребовалось, так как большинство разделов в Summary отмечены, как корректно выполненные. 
   * Summary
      ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ 
      --- | --- | --- 
      ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/YIE_summary.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/KAA_summary.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NPZ_summary.png)
   
   * Basic statistics
      ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ 
      --- | --- | --- 
      ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/YIE_bas_stat.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/KAA_bas_stat.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NPZ_bas_stat.png)
    
    * Per tile sequence quality
      ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ 
      --- | --- | --- 
      ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/YIE_per_tile_seq_q.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/KAA_per_tile_seq_q.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NPZ_per_tile_seq_q.png)
      
    * Per base sequence content
      ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ 
      --- | --- | --- 
      ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/YIE_per_base_seq_content.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/KAA_per_base_seq_content.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NPZ_per_base_seq_content.png)
      
   * Per sequence GC content
      ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ 
      --- | --- | --- 
      ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/YIE_per_seq_GC_content.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/KAA_per_seq_GC_content.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NPZ__per_seq_GC_content.png)
