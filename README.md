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
      
   Вывод: Из данных таблиечк можем сделать вывод, что большинство анализов проведены корректно.
   
   * Basic statistics
      ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ 
      --- | --- | --- 
      ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/YIE_bas_stat.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/KAA_bas_stat.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NPZ_bas_stat.png)
  
  Вывод: В данных таблицах представлена базовая информация FASTQ файле. На мой взгляд информативными показателями являются: общее количество чтений, длина чтения и содержание GC.
    
   * Per tile sequence quality
      ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ 
      --- | --- | --- 
      ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/YIE_per_tile_seq_q.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/KAA_per_tile_seq_q.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NPZ_per_tile_seq_q.png)
      
   Вывод: Данные графики позволяют посмотреть на средние показатели качества по всем данным, чтобы увидеть, не было ли потери качества, связанного только с одной частью. Можно заметить, что результаты во всех трех экспериментах, включая контрольный, оказались практически идеальными. Отличается от других лишь второй график (образец ENCFF826KAA), на котором видно несколько светлых частей, сигнализирующих о том, что в данных позициях качество было на уровне или выше среднего. Однако все значения в пределах нормы, большой потери качества не наблюдается.
      
   * Per base sequence content
      ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ 
      --- | --- | --- 
      ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/YIE_per_base_seq_content.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/KAA_per_base_seq_content.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NPZ_per_base_seq_content.png)
      
   Вывод: Можем заметить, что уровень Аденина(А), Гуанина(G), Цитозина(C), Тимина(T) остается на одном уровне, причем азотистые основания разбились на две группы тимин, аденин и цитозин, гуанин. Данное наблюдение прослеживается на всех трех графиках и свидетельствует о нормальных (не аномальных) значениях показателей.
      
   * Per sequence GC content
      ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ 
      --- | --- | --- 
      ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/YIE_per_seq_GC_content.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/KAA_per_seq_GC_content.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NPZ_per_seq_GC_content.png)
      
   Вывод: Исходя из трех скриншотов, видно, что на третьем графике кривые похожи на нормально распредление, где среднее значение соотвествует среднему содержанию GC в секвинируемом огранизме. Для первых двух скриншотов, можно же заметить, что их распредление откличается от нормального, в связи с чем в таблице Summary напротив данного параметра мы наблюдаем восклицательный знак, сигнализирующий о возможных проблемах при данном анализе.
  
---
2.

