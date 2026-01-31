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

#include <libopencm3/stm32/rcc.h>  // Header file for clock configuration (rcc clock)
#include <libopencm3/stm32/gpio.h>

#define LED_PORT (GPIOA)
#define LED_PIN  (GPIO5)
static void rcc_setup(void) // This function is visible and available ONLY to this translation unit i.e., this C file + included Header files
 {
    rcc_clock_setup_pll(&rcc_hsi_configs[RCC_CLOCK_3V3_84MHZ]);  // Set the CPU clock and frequency and the hardware that sets up that clock frquency (phase locked loop)
}   

static void gpio_setup(void) {
    rcc_periph_clock_enable(RCC_GPIOA);
    gpio_mode_setup(GPIOA, GPIO_MODE_OUTPUT, GPIO_PUPD_NONE, GPIO5);

}
static void delay_cycles(uint32_t cycles) {
    for (uint32_t i = 0; i < cycles; i++) {
        __asm__("nop");
    }
}

int main(void) {
    rcc_setup();
    gpio_setup();

    while (1) {
        gpio_toggle(LED_PORT, LED_PIN);
        delay_cycles(84000000 / 4);

    }


    //Never return
    return 0;
}

