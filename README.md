# Jarkom-Modul-1-I05-2023

## Modul 1 Jarkom 2023 I05 Formal Report

Group Members:
| No |  Name    |  NRP  |
| ---       |   ---     |---  |
|     1     |     Khairiya Maisa Putri    | 5025211192 |
|     2     |     Talitha Hayyinas Sahala    |  5025211263 |

# No. 1
## Question
> User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

In this task, We have to identify user activity focused on the action of ```uploading a file```. Therefore, we can trace packets that contain requests and responses related to this activity by filtering for = ftp. This information can be found in packets number ```147``` and ```149``` which are zip files.

> a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?

**answer:** ```258040667```

To obtain this information, we need to examine the ```Transmission Control Protocol``` section of packet ```147``` that is available. By doing this, we will be able to find the needed answer, which is ```258040667```.

<img width="1440" alt="Screen Shot 2023-09-22 at 16 43 42" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/df5b5640-658e-483a-9ecd-42b57d1b93c3">


> b.  Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?

**answer:** ```1044861039```

In the same section, you can find the ```Acknowledgment number (raw)``` following the previously mentioned value, and its value is ```1044861039```.

<img width="1440" alt="Screen Shot 2023-09-22 at 16 43 42" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/81570c66-0a8a-4a8a-833e-9f2a0ee912fa">


> c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

**answer:** ```1044861039```

This is similar to question `a`, but we need to look for the  ```STOR``` operation in packet number ```149```. And we got ```1044861039```.

<img width="1440" alt="Screen Shot 2023-09-22 at 16 44 00" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/48a0d73d-5fdd-415e-94bc-6cc23913d22d">


> d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

**answer:** ```258040696```

This also similar to question `b`, and also need to look for the  ```STOR``` operation in packet number ```149```. And we got ```258040696```.

<img width="1440" alt="Screen Shot 2023-09-22 at 16 44 00" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/cb920302-9ecc-48c6-9c4b-20ac8a313c1d">

**Terminal:**

<img width="1281" alt="Screen Shot 2023-09-22 at 16 45 15" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/432e756c-13fe-4910-bfb7-3cbc015b5192">

# No. 2
## Question
> Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

**answer:** ```gunicorn```

**Wireshark:**

<img width="1440" alt="Screenshot 2023-09-18 at 19 57 38" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/47e75054-4d20-406c-a30a-116768ff629d">


**Terminal:**

<img width="562" alt="Screenshot 2023-09-18 at 19 58 23" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/32031474-7604-4ee2-abf9-8a148b3209f2">


## Explanation
To find the web server that the practicum portal used, I filtered the packets using ```http``` on the file that was given. After that, I search for the same IP address as the portal, which is on the no 1765. Then, I double clicked on it and all of the details will come up at the bottom of the screen (the black part on the wireshark screen). And then we can see the the server that is used under the _Hypertext Transfer Protocol,_ which is ```gunicorn```.

# No. 3
## Question
>a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

**answer:** ```21```

>b. Protokol layer transport apa yang digunakan?

**answer:** ```UDP```

**Wireshark:**

<img width="1440" alt="Screen Shot 2023-09-22 at 16 52 47" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/3546ccb9-6675-4c46-8f68-4a8c75c5edfd">

**Terminal:**

<img width="1440" alt="Screen Shot 2023-09-22 at 16 52 55" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/b9f41f00-8d6c-4934-bc41-27b41dbc2e71">


## Explanation
a. To do this question, we can use a query filter.  We use ip.src or ip.dst for the address and udp.port for the desired port. In this context, we need to apply the filter query (ip.src == 239.255.255.250 or ip.dst == 239.255.255.250) && udp.port == 3702. The result will display all packets that match the filter query. After counting, the total is 21 packets.

## Explanation
b. for this question we can see the protocol inside the protocol column, and it shows UDP.

# No. 4
## Question
> Berapa nilai checksum yang didapat dari header pada paket nomor 130?

**answer:** ```0x18e5```

**Wireshark:**

<img width="1440" alt="4" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/3fa09d5b-36b1-4d36-b1d7-0571b0ee702d">


**Terminal:**

<img width="568" alt="4 terminal" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/30d195ca-34e4-4e5d-9f1b-9b7498972412">


## Explanation
To find the checksum value on the packet no 130, first I opened the file that was given. Then, I searched for the packet no 130 and double clicked it. And we will see the checksum value under the _User Datagram Protocol_, which is ```0x18e5```.

# No. 5
## Question
> a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?

**answer:** ```60```
> b. Port berapakah pada server yang digunakan untuk service SMTP?

**answer:** ```25```
> c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

**answer:** ```74.53.140.153```

**Wireshark:**

<img width="1440" alt="5 wireshark" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/6035b54a-dee8-4e6e-ada7-750b8888942c">

<img width="1440" alt="5 password" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/517ce155-991c-49da-a68b-19e1851732d5">


**To decode the zip password:**

<img width="904" alt="5 decode" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/492f172b-ffde-45cd-8a71-d93358375af7">

**Inside of the zip file:**

<img width="1440" alt="5 file buat instance" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/cb5c0028-88ac-46e5-b7aa-228493589161">

**To find the answers for the questions on the terminal:**

<img width="1440" alt="5 answers" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/ad1da252-8b4f-4b85-aa92-e499d81ba990">

**Terminal:**

<img width="620" alt="5 terminal" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/6f66e3cd-c8ae-4f43-af1b-a1747d84de80">

## Explanation
For this answer we were given 2 files, which are a  **zip** file, and a **pcap** file. To open the zip file we have to find its password using the pcap file. First I filtered all the packets using ```tcp.stream eq 0``` and then search for the packet that has _pass_ in it. Then I right cliked and choose ```Follow``` then ```TCP Stream```. It will open a new window, and you will find the password which is ```NWltcGxlUGFzNXdvcmQ=```, but you will still need to decode it in order to use it to open the zip file. Since it says that it needs to be decoded from Base64, I used a website where it can decode from Base64. After decoding it, I got the real password that can be used to open the zip file which is ```5implePas5word```. After successfully open the zip file, it will show the **instance** that we can copy and paste to the terminal to get the questions that we need to answer. 

# No. 6
## Question
> Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

**answer:** ```JDRNJA```

**Wireshark:**

<img width="1440" alt="Screen Shot 2023-09-22 at 16 55 21" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/a9cba12b-db07-41a8-9c71-cc413228157a">

**Terminal:**

<img width="1440" alt="Screen Shot 2023-09-22 at 16 57 48" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/0cca97ac-4fe8-497b-ad10-78af29b76f2b">

## Explanation

Our task here is to find the packet with the ```sequence number``` ```7812```.
we need to concentrate on the term ```SOURCE ADDRESS```, which refers to the source address in ```IP source``` format mentioned in the information. Then convert the sequence of numbers from this source address into several numbers, considering that we only have ```26``` letters from the substitution result in the alphabet.

Combine the source IP address that we found in packet ```7812```. Which here, we got ```1041814101```.

Then we can break it down into numbers that are <= 26, like this ```10 4 18 14 10 1```. Finally, we can form a word using the pattern that has been found, which is ```JDRNJA```. 

# No. 7
## Question
> Berapa jumlah packet yang menuju IP 184.87.193.88?

**answer:** ```6```

**Wireshark:**

<img width="1440" alt="7 wireshark" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/1abc3f11-e2fb-476e-81dd-5881fa1397a1">

**Terminal:**

<img width="506" alt="7 terminal" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/7634c1ec-c27d-42e2-83d9-a5b9309b8fdc">

## Explanation
For this question, we were asked the amout of packets that the **destination IP** is **184.87.193.88**. To get the amount of packets, I filtered it using ```ip.dst == 184.87.193.88``` on the **pcapng** file. After finished filtering, we can see at the bottom right that the amount of packets are ```6```.

# No. 8
## Question
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

**answer:** ```tcp.dstport == 80 || udp.dstport == 80```

**Wireshark:**

<img width="1440" alt="Screen Shot 2023-09-22 at 16 58 59" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/f6744e08-6e72-48a5-b880-7d6f0d54a67a">


**Terminal:**

<img width="1440" alt="Screen Shot 2023-09-22 at 16 59 05" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/f3b72db6-df1f-4f33-afa2-d552c44e7b3c">



## Explanation

In this task, we were asked to query a filter so that Wireshark only captures all protocol packets destined for ```port 80!``` (If there are multiple ports, sort them alphabetically). To achieve this, we can use the following Wireshark filter query: ```tcp.dstport == 80 || udp.dstport == 80```. By using this filter query, Wireshark will display all packets directed to port 80, whether they are using the ```TCP or UDP``` protocol.

# No. 9
## Question
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

**answer:** ``` ip.src == 10.51.40.1 && ip.dst != 10.39.55.34```

**Wireshark:**

<img width="1440" alt="Screen Shot 2023-09-22 at 17 00 16" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/856227f4-d86d-400a-80c3-7e70680fd91d">

**Terminal:**

<img width="1440" alt="Screen Shot 2023-09-22 at 16 59 59" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/90357502/1c954d5a-2465-42b3-b273-a633ec771e9d">


## Explanation

We were asked to provide a filter query so that Wireshark only captures packets originating from the address ```10.51.40.1``` but not destined for the address ```10.39.55.34!``` To achieve this, we can use the following Wireshark filter query: ```ip.src == 10.51.40.1 && ip.dst != 10.39.55.34```. When we combine these two conditions, we’ll get a filter query that captures packets sent from 10.51.40.1 to any destination except 10.39.55.34.

# No. 10
## Question
> Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

**answer:** ```dhafin:kesayangannyak0k0```

**Wireshark:**

<img width="1440" alt="10 wireshark" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/b101e644-3f80-4cd7-a314-17c55a832b34">

**To get the username and password as the answer for the question:**

<img width="1440" alt="10 file jawaban" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/2c212439-c0d7-46ed-8b4a-80d24e7a2822">

**Terminal:**

<img width="563" alt="10 terminal" src="https://github.com/khairiyaputrii/Jarkom-Modul-1-I05-2023/assets/115809934/beaaaab7-2080-455a-b00b-3a264651f1ef">

## Explanation
For this question we were asked to find the username and password of the user in the format ```username:password``` using Telnet. To get the answer first thing that I did was filter all the packets using ```telnet```, and then I choose the pack **no 262**. Then I right click on that packet, and choose ```Follow``` then ```TCP Stream```. It will open a new window, and you will find the username and password which are ```ddhhaaffiinn``` and ```kesayangannyak0k0```. Since the username is 2 colors, blue and red, and the password is only in one color, red, I only take the red letters for the username, which is ```dhafin```. That is how I get the answer as ```dhafin:kesayangannyak0k0```.
