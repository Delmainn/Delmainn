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


delmain@Xubuntu:~/Bare-Bootloader/app$ ls -la ../libopencm3/lib/libopencm3_stm32f4.a 
-rw-rw-r-- 1 delmain delmain 3910454 Jan 30 15:26 ../libopencm3/lib/libopencm3_stm32f4.a
delmain@Xubuntu:~/Bare-Bootloader/app$ make -n src/firmware.o
#printf "  CC      src/firmware.c\n"
arm-none-eabi-gcc -Os -std=c99 -ggdb3 -mthumb -mcpu=cortex-m4 -mfloat-abi=hard -mfpu=fpv4-sp-d16 -Wextra -Wshadow -Wimplicit-function-declaration -Wredundant-decls -Wmissing-prototypes -Wstrict-prototypes -fno-common -ffunction-sections -fdata-sections  -MD -Wall -Wundef -DSTM32F4 -I../libopencm3/include -Iinc -I../shared/inc  -o src/firmware.o -c src/firmware.c
