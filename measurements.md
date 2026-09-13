# FormFactor measurements

## 2026-09-11 — Baseline, generated code only

CubeMX generated project, nothing written yet. Built clean, 0 errors 0 warnings.

Clock (verified in CubeMX clock configuration):
- HSE 8 MHz, PLL /16 x336 /4, SYSCLK 84 MHz
- HCLK 84 MHz, APB1 42 MHz, APB2 84 MHz

Size (arm-none-eabi-size):
- text 7712, data 12, bss 1644
- Flash used: 7724 B of 524288 (1.5%)
- RAM used: 1656 B of 98304 (1.7%)

Method: build console output, Debug configuration, -O0.

## 2026-09-13 — Phase 0 complete

LD2 (PA5) blinks at 1 Hz via HAL_GPIO_TogglePin + HAL_Delay(500).
Breakpoint set on the toggle line, hit under the debugger, single stepped
through several toggles and confirmed LD2 changes state on each resume.
Program persists in flash: reset restarts it with no debugger attached.

Size after adding the blink: 7.68 KB flash (was 7.54 KB generated only).
Delta ~140 B for the two lines plus the HAL functions they pull in.