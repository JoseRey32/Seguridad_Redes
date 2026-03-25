## Descripción

🥛

Additional details will be available after launching your challenge instance.

## Solucion 
```
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOni]
└─$ ..
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ mkdir milk        
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ cd milk        
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/milk]
└─$ wget http://wily-courier.picoctf.net:62219/concat_v.png
--2026-03-25 01:08:38--  http://wily-courier.picoctf.net:62219/concat_v.png
Resolving wily-courier.picoctf.net (wily-courier.picoctf.net)... 18.189.99.27
Connecting to wily-courier.picoctf.net (wily-courier.picoctf.net)|18.189.99.27|:62219... connected.
HTTP request sent, awaiting response... 200 OK
Length: 18095920 (17M) [image/png]
Saving to: ‘concat_v.png’

concat_v.png                           100%[===========================================================================>]  17.26M  1.05MB/s    in 9.2s    

2026-03-25 01:08:47 (1.88 MB/s) - ‘concat_v.png’ saved [18095920/18095920]

                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/milk]
└─$ zsteg              
Usage: zsteg [options] filename.png [param_string]

    -a, --all                        try all known methods
    -E, --extract NAME               extract specified payload, NAME is like '1b,rgb,lsb'

Iteration/extraction params:
    -o, --order X                    pixel iteration order (default: 'auto')
                                     valid values: ALL,xy,yx,XY,YX,xY,Xy,bY,...
    -c, --channels X                 channels (R/G/B/A) or any combination, comma separated
                                     valid values: r,g,b,a,rg,bgr,rgba,r3g2b3,...
    -b, --bits N                     number of bits, single int value or '1,3,5' or range '1-8'
                                     advanced: specify individual bits like '00001110' or '0x88'
        --lsb                        least significant bit comes first
        --msb                        most significant bit comes first
    -P, --prime                      analyze/extract only prime bytes/pixels
        --shift N                    prepend N zero bits
        --invert                     invert bits (XOR 0xff)
        --pixel-align                pixel-align hidden data

Analysis params:
    -l, --limit N                    limit bytes checked, 0 = no limit (default: 256)

        --[no-]file                  use 'file' command to detect data type (default: YES)
        --no-strings                 disable ASCII strings finding (default: enabled)
    -s, --strings X                  ASCII strings find mode: first, all, longest, none
                                     (default: first)
    -n, --min-str-len X              minimum string length (default: 8)

    -v, --verbose                    Run verbosely (can be used multiple times)
    -q, --quiet                      Silent any warnings (can be used multiple times)
    -C, --[no-]color                 Force (or disable) color output (default: auto)

PARAMS SHORTCUT
        zsteg fname.png 2b,b,lsb,xy  ==>  --bits 2 --channel b --lsb --order xy
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/milk]
└─$ zsteg -s all *.png mkdir milk                          
[.] concat_v.png
/var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:369:in `prev_scanline_byte': stack level too deep (SystemStackError)
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:319:in `block in decoded_bytes'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `upto'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `decoded_bytes'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line/mixins.rb:17:in `prev_scanline_byte'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:377:in `prev_scanline_byte'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:319:in `block in decoded_bytes'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `upto'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `decoded_bytes'
         ... 10225 levels...
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.14/lib/zsteg.rb:26:in `run'
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.14/bin/zsteg:8:in `<top (required)>'
        from /usr/local/bin/zsteg:25:in `load'
        from /usr/local/bin/zsteg:25:in `<main>'
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/milk]
└─$ zsteg -s all * .png mkdir milk
[.] concat_v.png
/var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:369:in `prev_scanline_byte': stack level too deep (SystemStackError)
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:319:in `block in decoded_bytes'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `upto'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `decoded_bytes'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line/mixins.rb:17:in `prev_scanline_byte'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:377:in `prev_scanline_byte'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:319:in `block in decoded_bytes'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `upto'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `decoded_bytes'
         ... 10225 levels...
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.14/lib/zsteg.rb:26:in `run'
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.14/bin/zsteg:8:in `<top (required)>'
        from /usr/local/bin/zsteg:25:in `load'
        from /usr/local/bin/zsteg:25:in `<main>'
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/milk]
└─$ zsteg -s all *.png mkdir milk 
[.] concat_v.png
/var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:369:in `prev_scanline_byte': stack level too deep (SystemStackError)
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:319:in `block in decoded_bytes'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `upto'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `decoded_bytes'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line/mixins.rb:17:in `prev_scanline_byte'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:377:in `prev_scanline_byte'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:319:in `block in decoded_bytes'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `upto'
        from /var/lib/gems/3.3.0/gems/zpng-0.4.6/lib/zpng/scan_line.rb:318:in `decoded_bytes'
         ... 10225 levels...
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.14/lib/zsteg.rb:26:in `run'
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.14/bin/zsteg:8:in `<top (required)>'
        from /usr/local/bin/zsteg:25:in `load'
        from /usr/local/bin/zsteg:25:in `<main>'
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/milk]
└─$ 

```
No pude resolver ese error se supone que después de eso da la bandera 