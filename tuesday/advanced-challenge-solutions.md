    cat BSD | sed 's/ //g'
    zcat C61_S67_L006_R1_001.fastq.gz | sed -n '2~4p' | cut -c1-5 | sort | uniq -c
    find /software/perl-libs/ -name "*.pm" | while read x; do grep -H -w -i blast $x; done
    zcat C61_S67_L006_R1_001.fastq.gz | grep -E 'A{7,16}$'
    find -L /share/biocore/joshi/projects/genomes -maxdepth 7 -name "*.fa" | grep -E 'ce10|danRer7' | xargs wc -c | awk '$1<10000'
