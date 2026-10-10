```text
Why is a Subnet Mask Important? (বাংলায় ব্যাখ্যা)
Subnet Mask গুরুত্বপূর্ণ, কারণ এটি কম্পিউটারকে বুঝতে সাহায্য করে IP Address-এর কোন অংশ Network এবং কোন অংশ Host নির্দেশ করে।
1. Identify Network (Network শনাক্ত করা)
Subnet Mask ব্যবহার করে একটি IP Address-এর Network Address নির্ধারণ করা যায়।
Example:
IP Address   : 192.168.1.10
Subnet Mask  : 255.255.255.0
Network      : 192.168.1.0


এখানে 192.168.1 হলো Network portion এবং 10 হলো Host portion।
অর্থাৎ, কম্পিউটার বুঝতে পারে ডিভাইসটি কোন Network-এর অন্তর্ভুক্ত।
2. Communication (ডিভাইসের মধ্যে যোগাযোগ)
Subnet Mask নির্ধারণ করতে সাহায্য করে দুটি ডিভাইস একই subnet-এ আছে কি না।
PC A
IP: 192.168.1.10
Mask: 255.255.255.0

Same Subnet
Local network-এর মাধ্যমে যোগাযোগ

PC B
IP: 192.168.1.20
Mask: 255.255.255.0


দুটি কম্পিউটারের Network Address 192.168.1.0। তাই তারা একই subnet-এ আছে এবং সাধারণত Router ছাড়াই একই LAN-এ যোগাযোগ করতে পারে।
3. Routing (সঠিক পথে Data পাঠানো)
কম্পিউটার যখন অন্য একটি IP Address-এ data পাঠাতে চায়, তখন Subnet Mask ব্যবহার করে বুঝতে পারে Destination একই subnet-এ নাকি অন্য subnet-এ।
Source PC
192.168.1.10/24

Destination IP পরীক্ষা

Same subnet
192.168.1.20
Direct via LAN


Different subnet
192.168.2.20
Via Router




উদাহরণে Source PC-এর IP 192.168.1.10/24।
- Destination 192.168.1.20 হলে, এটি একই subnet-এ। PC সাধারণত সরাসরি LAN-এর মাধ্যমে পাঠায়।
- Destination 192.168.2.20 হলে, এটি অন্য subnet-এ। PC সাধারণত Default Gateway-তে packet পাঠায়।
4. Subnetting (বড় Network-কে ছোট Network-এ ভাগ করা)
Subnet Mask ব্যবহার করে একটি বড় Network-কে একাধিক ছোট Network-এ ভাগ করা যায়।
উদাহরণ: 192.168.1.0/24 Network-এ মোট 254টি সাধারণ usable host address আছে।
এটিকে /25 দিয়ে দুটি subnet-এ ভাগ করলে:
Subnet	Usable Host Range	Hosts
192.168.1.0/25	192.168.1.1–126	126
192.168.1.128/25	192.168.1.129–254	126
এতে একটি প্রতিষ্ঠানের HR Department এবং IT Department-এর জন্য আলাদা subnet তৈরি করা যায়।


```
