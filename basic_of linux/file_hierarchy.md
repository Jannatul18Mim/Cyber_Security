## **Architecture of File System** 

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20260112171619580125/the_architecture_of_a_file_system.webp" alt="Architecture of file system">
</P>

---    

## **Types of Linux File System**

<p align="center">
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20260110115203625332/file.webp" alt="Types of linux File System">
</p>

---  

## **Linux File Hierarchy Structure:**


<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20260108164511372024/Linux_File_Hierarchy.webp" alt="Linux File Hierarchy">
</p>


---

## **🐧 Linux Fundamentals: Console, Terminal, Shell & Kernel**

🍽️ রেস্টুরেন্ট এনালজি (সহজ উদাহরণ)

  Console (পুরো রেস্টুরেন্ট বিল্ডিং): যে প্রধান পরিকাঠামো বা হার্ডওয়্যারের ওপর দাঁড়িয়ে সবকিছু চলছে।

  Terminal (টেবিল/মেনু কার্ড): যেখানে তুমি বসে আছো এবং অর্ডারটা লিখছো। এটি তোমার সামনে থাকা ইন্টারফেস।

  Shell (ওয়েটার): যে তোমার অর্ডারটা (Command) বুঝে রান্নাঘরে নিয়ে যায়। সে তোমার ভাষা বোঝে এবং সেটা শেফকে বুঝিয়ে বলে।
    
  Kernel (শেফ/বাবুর্চি): যে আসলে খাবারটা রান্না করে (Hardware-কে কাজ করায়)। সে কিন্তু সরাসরি কাস্টমারের সাথে কথা বলে না।

📝 মূল বিষয়সমূহ (Core Concepts)
১. Console (The Physical Interface)

  কি: এটি সরাসরি কম্পিউটারের সাথে যুক্ত একটি ফিজিক্যাল ডিভাইস। প্রাচীনকালে এটি ছিল একটি মনিটর এবং কিবোর্ড যা দিয়ে 
  সরাসরি মেইনফ্রেম  কম্পিউটার কন্ট্রোল করা হতো।

  কাজ: সিস্টেমের একদম প্রাথমিক পর্যায়ের ইনপুট এবং আউটপুট সরাসরি হ্যান্ডেল করা।

২. Terminal (The Gateway)

  কি: এটি একটি উইন্ডো বা সফটওয়্যার প্রোগ্রাম (যেমন: GNOME Terminal) যেখানে আমরা কমান্ড টাইপ করি।

  কাজ: ইউজারের কাছ থেকে ইনপুট নেওয়া এবং স্ক্রিনে রেজাল্ট বা আউটপুট দেখানো। এটি মূলত একটি Input/Output মাধ্যম।

৩. Shell (The Interpreter)

  কি: এটি একটি প্রোগ্রাম যা টার্মিনাল থেকে কমান্ডগুলো পড়ে এবং সেগুলোকে কার্নেলের বোঝার উপযোগী ভাষায় অনুবাদ করে।

  কাজ: কমান্ডের সিনট্যাক্স চেক করা এবং কার্নেলকে কাজের নির্দেশ দেওয়া।

  উদাহরণ: Bash, Zsh।

৪. Kernel (The Core)

  কি: এটি অপারেটিং সিস্টেমের হৃৎপিণ্ড বা মস্তিস্ক।

  কাজ: সরাসরি হার্ডওয়্যারের (RAM, CPU, Disk) সাথে যোগাযোগ করা এবং কাজ সম্পন্ন করা।

  নিরাপত্তা: ইউজার কখনো সরাসরি কার্নেলকে অ্যাক্সেস করতে পারে না, মাঝখানে নিরাপত্তা নিশ্চিত করে Shell।

🔄 কাজের ধাপ (Workflow)

ইউজার (কমান্ড দিল) ➔ Terminal ➔ Shell (অনুবাদ করল) ➔ Kernel ➔ Hardware (কাজ সম্পন্ন হলো)

