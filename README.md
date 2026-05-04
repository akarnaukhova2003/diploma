# Astroviridae | diploma 
В данном репозитории представлены скрипты и иные дополнительные материалы по дипломной работе
### Скрипты (папка scripts)
* get_lineages_rank.py (Скрипт получает таксономическую линию (lineage) для списка организмов-хостов из NCBI Taxonomy)

```
Аргументы:
  -i, --input   Входной CSV-файл (обязательно, должен содержать колонку "Host")
  -o, --output  Выходной CSV-файл (по умолчанию: hosts_lineage_rank.csv)
```
* get_orfs.py заимствован у коллег: https://github.com/v-julia/GenAlignment/blob/master/get_orfs.py
* split_genome_and_reverse.py
```
Скрипт разбивает геномы из FASTA на ORF-последовательности по координатам, если встречает '-' цепь, то последовательность реверс-комплементируется.
Аргументы:
  -i, --input    Входной FASTA-файл (обязательно)
  -c, --coords   CSV-файл с координатами ORF и strand (обязательно)  
```

* filter_fasta_by_length.py
```
Скрипт фильтрует последовательности FASTA по длине.
Аргументы:
  -i, --input     Входной FASTA-файл (обязательно)
  -o, --output    Выходной FASTA-файл (обязательно)
  -m, --min-len   Минимальная длина последовательности (обязательно)
      --max-len   Максимальная длина (необязательно)
```

* resolve_ambiguous_mac.py заимствован у коллег: https://github.com/v-julia/resolve_ambiguous/blob/master/resolve_ambiguous.py
* extract_fasta_from_treefile.py
```
Скрипт извлекает последовательности из FASTA на основе цвета кластеров в дереве.
Аргументы:
  --tree        Файл дерева с taxlabels (обязательно)
  --clusters    TSV-файл кластеров (обязательно)
  --color       Цвет для отбора (обязательно)
  --fasta       Входной FASTA (обязательно)
  --out_ids     Выходной файл со списком ID
  --out_fasta   Выходной FASTA
```

* join_al.py заимствован у коллег: https://github.com/v-julia/GenAlignment/blob/master/join_al.py

### Файлы (папка files)
* Astroviridae_15102025.fasta (нуклеотидные последовательности семейства *Astroviridae*, полученные 15.10.2025
* Astroviridae_15102025.gb (записи о каждой последовательности в формате .gb)
* Astroviridae_15022026_orf-coords.csv (файл с координатами рамок, включая исправленные и дополненные)
* Astroviridae_15102025.csv (файл с метаданными в формате .csv)
* Astroviridae_20042026_full.csv (расширенный файл - добавлено название класса хозяева и координаты кодирующих рамок)
* Astroviridae_Aves_03052026_clusters_shorter.csv (файл с номера кластеров при различных порогах кластеризации для представителей клады птиц)


### Деревья
* в папке tree_aves представлены деревья, построенные по расширенной выборке клады птиц для ORF1a, ORF1b и ORF2
