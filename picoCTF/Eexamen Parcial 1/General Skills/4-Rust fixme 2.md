## Descripción

The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).

## Solucion 

```
┌──(kali㉿kali)-[~]
└─$ ls    
Desktop  Documents  Downloads  fixme1  fixme1.tar  Music  picoctf  Pictures  Public  Templates  Videos
                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ wget https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz
--2026-03-25 19:11:25--  https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.161.44.61, 3.161.44.22, 3.161.44.103, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.161.44.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1585 (1.5K) [application/octet-stream]
Saving to: ‘fixme2.tar.gz’

fixme2.tar.gz                          100%[===========================================================================>]   1.55K  --.-KB/s    in 0s      

2026-03-25 19:11:25 (7.92 MB/s) - ‘fixme2.tar.gz’ saved [1585/1585]

                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$  tar -xvzf fixme2.tar.gz
fixme2/
fixme2/Cargo.toml
fixme2/Cargo.lock
fixme2/src/
fixme2/src/main.rs
                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ ls 
Desktop  Documents  Downloads  fixme1  fixme1.tar  fixme2  fixme2.tar.gz  Music  picoctf  Pictures  Public  Templates  Videos
                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ cd fixme2
                                                                                                                                                           
┌──(kali㉿kali)-[~/fixme2]
└─$ ls
Cargo.lock  Cargo.toml  src
                                                                                                                                                           
┌──(kali㉿kali)-[~/fixme2]
└─$ cd src   
                                                                                                                                                           
┌──(kali㉿kali)-[~/fixme2/src]
└─$ cd ..     
                                                                                                                                                           
┌──(kali㉿kali)-[~/fixme2]
└─$ ls
Cargo.lock  Cargo.toml  src
                                                                                                                                                           
┌──(kali㉿kali)-[~/fixme2]
└─$ cargo run main
   Compiling crossbeam-utils v0.8.20
   Compiling rayon-core v1.12.1
   Compiling either v1.13.0
   Compiling crossbeam-epoch v0.9.18
   Compiling crossbeam-deque v0.8.5
   Compiling rayon v1.10.0
   Compiling xor_cryptor v1.2.3
   Compiling rust_proj v0.1.0 (/home/kali/fixme2)
error[E0596]: cannot borrow `*borrowed_string` as mutable, as it is behind a `&` reference
 --> src/main.rs:9:5
  |
9 |     borrowed_string.push_str("PARTY FOUL! Here is your flag: ");
  |     ^^^^^^^^^^^^^^^ `borrowed_string` is a `&` reference, so the data it refers to cannot be borrowed as mutable
  |
help: consider changing this to be a mutable reference
  |
3 | fn decrypt(encrypted_buffer:Vec<u8>, borrowed_string: &mut String){ // How do we pass values to a function that we want to change?
  |                                                        +++

error[E0596]: cannot borrow `*borrowed_string` as mutable, as it is behind a `&` reference
  --> src/main.rs:20:5
   |
20 |     borrowed_string.push_str(&String::from_utf8_lossy(&decrypted_buffer));
   |     ^^^^^^^^^^^^^^^ `borrowed_string` is a `&` reference, so the data it refers to cannot be borrowed as mutable
   |
help: consider changing this to be a mutable reference
   |
 3 | fn decrypt(encrypted_buffer:Vec<u8>, borrowed_string: &mut String){ // How do we pass values to a function that we want to change?
   |                                                        +++

For more information about this error, try `rustc --explain E0596`.
error: could not compile `rust_proj` (bin "rust_proj") due to 2 previous errors
                                                                                                                                                           
┌──(kali㉿kali)-[~/fixme2]
└─$ cd src        
                                                                                                                                                           
┌──(kali㉿kali)-[~/fixme2/src]
└─$ nano main.rs 
                                                                                                                                                           
┌──(kali㉿kali)-[~/fixme2/src]
└─$ cd .. 
                                                                                                                                                           
┌──(kali㉿kali)-[~/fixme2]
└─$ cargo run main
   Compiling rust_proj v0.1.0 (/home/kali/fixme2)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.24s
     Running `target/debug/rust_proj main`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{4r3_y0u_h4v1n5_fun_y31?}

```