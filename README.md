# hse_hw2_chip

[Ссылка на колаб](https://colab.research.google.com/drive/1cnSsux6vQHfxGYYd3DwXDIJ9jJ8b69io?usp=sharing)<br>
[Ссылка на условия](https://docs.google.com/document/d/1bPVShA20DJureQI5SPLIb8_Ls3vTnrX46WunIZkpgFk/edit)

---
Клеточная линия | Гистоновая метка | Реплика 1 | Реплика 2 | Контрольный эксперимент 
--- | --- | --- | --- | ---
A549 | H3K4me2 | ENCFF507YIE | ENCFF826KAA | ENCFF232NPZ

---
1. Отчеты Fastqc
 
   При анализе Fastqc подрезание прочтений и фильтрация не потребовалось, так как большинство разделов в Summary отмечены, как корректно выполненные. 
   
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
2. Таблица со статистикой по каждому из 3 образцов

  Образец | Всего ридов | Выровнилось уникально | Выровнилось уникально(%) |	Выровнилось неуникально | Выровнилось неуникально(%) | Не выровнилось | Не выровнилось(%)
  --- | --- | --- | --- | --- | --- | --- | --- 
  ENCFF507YIE | 45551674 | 1278836 | 2.81% | 4569570 | 10.03% | 39703268	| 87.16%
  ENCFF826KAA	| 46522698 | 1129018	| 2.43%	| 3765869	| 8.09%	| 41627811	| 89.48%
  ENCFF232NPZ	| 26282868 | 865880	| 3.29%	| 3363247 |	12.80%	| 22053741	| 83.91%

  Вывод: Процент выравниваний получился низким, так как выравнивание ридов производилось на одну хромосому, которая составляет небольшую часть генома человека.
  
---
3. Диаграммы Венна
   
  * Для образца ENCFF507YIE
     Количество участков из файла для ENCFF507YIE, которые пересекаются с файлом для ENCFF806AQL  | Количество участков из файла для ENCFF806AQL, которые пересекаются с файлом для ENCFF507YIE
     --- | --- 
     ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/YIE_with_AQL.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/AQL_with_YIE.png)
     
  * Для образца ENCFF826KAA
     Количество участков из файла для ENCFF826KAA, которые пересекаются с файлом для ENCFF806AQL  | Количество участков из файла для ENCFF806AQL, которые пересекаются с файлом для ENCFF826KAA
     --- | --- 
     ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/KAA_with_AQL.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/AQL_with_KAA.png)

Наблюдение: исходя из диаграмм видно, что количество пересекающихся учатсков относительно небольшое. Скорее всего это произошло из-за того, что изначально у нас было относительно не большое количество пиков, так как выравнивание производилось только на одну хромосому. Для файла ENCFF806AQL, взятого из ENCODE, количество пиков же гораздо больше, в связи с выравниванием на все хромосомы. Можно также заметить, что пересечения на двух графиках в одной таблице не совпадают, в силу того как было опредлено пересечение.

---
4. Бонусная часть
    Хитмэпы для bam файлов и соотвествующих им .bigWig файлов
    
    ngs.plot для ENCFF066HKS.bam | ngs.plot для ENCFF346XTR.bam
     --- | --- 
     ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/NIR.png) | ![](https://github.com/ulvivl/hse_hw2_chip/blob/main/img/UVW.png)
     
Наблюдение: Полученные графики для .bam файлов похожи на типичное расположение гистоновой метки относительно генов. Однако кажется что наш график немного смещен влевую сторону, то етсь видно что вначале график претерпевает рост, а затем претерпевает более плавный спад, вто время как на графике с типичным расположением рост и спад более плавные и почти одинаковые. Таким образом, теоретическое расположения гистоновой метки относительно генов чуть отличается от полученного.
