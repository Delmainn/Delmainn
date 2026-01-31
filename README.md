- 👋 Hi, I’m @Delmainn
- 👀 I’m interested in embedded systems
- 🌱 I’m currently learning bare-metal programming in C on arm microcontrollers
- 💞️ I’m looking to collaborate on projects relating to microcontrollers that would take me from a beginner to a regular.
- 📫 How to reach me ---> I'm right here ;)
- 😄 Pronouns: Him/Himothy/Himalayas/Himmy Neutron/
- ⚡ Fun fact: I played Sax in high school

<!---
Delmainn/Delmainn is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

cd ~/Bare-Bootloader/app && \
echo "=== 1. Checking OBJS files ===" && \
ls -la src/*.c 2>/dev/null && \
echo "=== 2. Checking linker script ===" && \
ls -la linkerscript.ld && \
echo "=== 3. Checking elf rule indentation ===" && \
sed -n '/^elf:/,/^[^\t]/p' Makefile | cat -A
