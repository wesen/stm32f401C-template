CC=arm-none-eabi-gcc
AR=arm-none-eabi-ar

###########################################

vpath %.c Libraries/STM32F4xx_StdPeriph_Driver/src

CFLAGS  = -g -O2 -Wall
CFLAGS += -mlittle-endian -mthumb -mcpu=cortex-m4 -march=armv7e-m
CFLAGS += -mfpu=fpv4-sp-d16 -mfloat-abi=hard
CFLAGS += -ffreestanding -nostdlib
CFLAGS += -include stm32f4xx_conf.h 
CFLAGS += -I Libraries/CMSIS/Include 
CFLAGS += -I Libraries/CMSIS/Device/ST/stm32f4xx/Include 
CFLAGS += -I Libraries/stm32f4xx_StdPeriph_Driver/inc
CFLAGS += -I Libraries/STM32_USB_Device_Library/Core/inc
CFLAGS += -I Libraries/STM32_USB_Device_Library/Class/audio/inc
CFLAGS += -I Libraries/STM32_USB_Device_Library/Class/cdc/inc
CFLAGS += -I Libraries/STM32_USB_Device_Library/Class/dfu/inc
CFLAGS += -I Libraries/STM32_USB_Device_Library/Class/hid/inc
CFLAGS += -I Libraries/STM32_USB_Device_Library/Class/msc/inc
CFLAGS += -I Libraries/CMSIS/Include
CFLAGS += -I Libraries/STM32_USB_OTG_Driver/inc
CFLAGS += -D$(MCU)
CFLAGS += -DARM_MATH_CM4

SRCS = stm32f4xx_adc.c stm32f4xx_can.c \
	   stm32f4xx_crc.c \
       stm32f4xx_dac.c stm32f4xx_dbgmcu.c stm32f4xx_dma.c \
       stm32f4xx_exti.c stm32f4xx_flash.c stm32f4xx_gpio.c \
       stm32f4xx_i2c.c stm32f4xx_iwdg.c \
       stm32f4xx_pwr.c stm32f4xx_rcc.c stm32f4xx_rtc.c stm32f4xx_spi.c \
       stm32f4xx_syscfg.c stm32f4xx_tim.c stm32f4xx_usart.c \
       stm32f4xx_wwdg.c \
       system_stm32f4xx.c

SRCS += \
Libraries/CMSIS/Device/ST/STM32F4xx/Source/Templates/system_stm32f4xx.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_abs_f32.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_abs_q15.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_abs_q31.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_abs_q7.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_add_f32.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_add_q15.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_add_q31.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_add_q7.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_dot_prod_f32.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_dot_prod_q15.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_dot_prod_q31.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_dot_prod_q7.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_mult_f32.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_mult_q15.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_mult_q31.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_mult_q7.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_negate_f32.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_negate_q15.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_negate_q31.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_negate_q7.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_offset_f32.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_offset_q15.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_offset_q31.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_offset_q7.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_scale_f32.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_scale_q15.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_scale_q31.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_scale_q7.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_shift_q15.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_shift_q31.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_shift_q7.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_sub_f32.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_sub_q15.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_sub_q31.c \
Libraries/CMSIS/DSP_Lib/Source/BasicMathFunctions/arm_sub_q7.c \
Libraries/CMSIS/DSP_Lib/Source/CommonTables/arm_common_tables.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_conj_f32.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_conj_q15.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_conj_q31.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_dot_prod_f32.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_dot_prod_q15.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_dot_prod_q31.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mag_f32.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mag_q15.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mag_q31.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mag_squared_f32.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mag_squared_q15.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mag_squared_q31.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mult_cmplx_f32.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mult_cmplx_q15.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mult_cmplx_q31.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mult_real_f32.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mult_real_q15.c \
Libraries/CMSIS/DSP_Lib/Source/ComplexMathFunctions/arm_cmplx_mult_real_q31.c \
Libraries/CMSIS/DSP_Lib/Source/ControllerFunctions/arm_pid_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/ControllerFunctions/arm_pid_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/ControllerFunctions/arm_pid_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/ControllerFunctions/arm_pid_reset_f32.c \
Libraries/CMSIS/DSP_Lib/Source/ControllerFunctions/arm_pid_reset_q15.c \
Libraries/CMSIS/DSP_Lib/Source/ControllerFunctions/arm_pid_reset_q31.c \
Libraries/CMSIS/DSP_Lib/Source/ControllerFunctions/arm_sin_cos_f32.c \
Libraries/CMSIS/DSP_Lib/Source/ControllerFunctions/arm_sin_cos_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FastMathFunctions/arm_cos_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FastMathFunctions/arm_cos_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FastMathFunctions/arm_cos_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FastMathFunctions/arm_sin_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FastMathFunctions/arm_sin_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FastMathFunctions/arm_sin_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FastMathFunctions/arm_sqrt_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FastMathFunctions/arm_sqrt_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df1_32x64_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df1_32x64_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df1_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df1_fast_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df1_fast_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df1_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df1_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df1_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df1_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df1_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df2T_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_biquad_cascade_df2T_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_fast_opt_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_fast_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_fast_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_opt_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_opt_q7.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_partial_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_partial_fast_opt_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_partial_fast_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_partial_fast_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_partial_opt_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_partial_opt_q7.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_partial_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_partial_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_partial_q7.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_conv_q7.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_correlate_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_correlate_fast_opt_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_correlate_fast_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_correlate_fast_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_correlate_opt_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_correlate_opt_q7.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_correlate_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_correlate_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_correlate_q7.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_decimate_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_decimate_fast_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_decimate_fast_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_decimate_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_decimate_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_decimate_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_decimate_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_decimate_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_fast_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_fast_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_init_q7.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_interpolate_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_interpolate_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_interpolate_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_interpolate_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_interpolate_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_interpolate_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_lattice_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_lattice_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_lattice_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_lattice_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_lattice_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_lattice_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_q7.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_sparse_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_sparse_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_sparse_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_sparse_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_sparse_init_q7.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_sparse_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_sparse_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_fir_sparse_q7.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_iir_lattice_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_iir_lattice_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_iir_lattice_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_iir_lattice_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_iir_lattice_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_iir_lattice_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_norm_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_norm_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_norm_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_norm_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_norm_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_norm_q31.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_q15.c \
Libraries/CMSIS/DSP_Lib/Source/FilteringFunctions/arm_lms_q31.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_add_f32.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_add_q15.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_add_q31.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_inverse_f32.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_mult_f32.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_mult_fast_q15.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_mult_fast_q31.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_mult_q15.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_mult_q31.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_scale_f32.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_scale_q15.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_scale_q31.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_sub_f32.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_sub_q15.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_sub_q31.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_trans_f32.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_trans_q15.c \
Libraries/CMSIS/DSP_Lib/Source/MatrixFunctions/arm_mat_trans_q31.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_max_f32.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_max_q15.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_max_q31.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_max_q7.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_mean_f32.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_mean_q15.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_mean_q31.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_mean_q7.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_min_f32.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_min_q15.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_min_q31.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_min_q7.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_power_f32.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_power_q15.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_power_q31.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_power_q7.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_rms_f32.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_rms_q15.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_rms_q31.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_std_f32.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_std_q15.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_std_q31.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_var_f32.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_var_q15.c \
Libraries/CMSIS/DSP_Lib/Source/StatisticsFunctions/arm_var_q31.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_copy_f32.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_copy_q15.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_copy_q31.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_copy_q7.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_fill_f32.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_fill_q15.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_fill_q31.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_fill_q7.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_float_to_q15.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_float_to_q31.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_float_to_q7.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_q15_to_float.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_q15_to_q31.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_q15_to_q7.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_q31_to_float.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_q31_to_q15.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_q31_to_q7.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_q7_to_float.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_q7_to_q15.c \
Libraries/CMSIS/DSP_Lib/Source/SupportFunctions/arm_q7_to_q31.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_bitreversal.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix2_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix2_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix2_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix2_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix2_q15.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix2_q31.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix4_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix4_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix4_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix4_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix4_q15.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix4_q31.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_cfft_radix8_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_dct4_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_dct4_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_dct4_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_dct4_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_dct4_q15.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_dct4_q31.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_rfft_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_rfft_fast_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_rfft_fast_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_rfft_init_f32.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_rfft_init_q15.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_rfft_init_q31.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_rfft_q15.c \
Libraries/CMSIS/DSP_Lib/Source/TransformFunctions/arm_rfft_q31.c \

SRCS +=
#Libraries/STM32_USB_Device_Library/Class/audio/src/usbd_audio_core.c \
#Libraries/STM32_USB_Device_Library/Class/audio/src/usbd_audio_out_if.c \
#Libraries/STM32_USB_Device_Library/Class/cdc/src/usbd_cdc_core.c \
#Libraries/STM32_USB_Device_Library/Class/cdc/src/usbd_cdc_if_template.c \
#Libraries/STM32_USB_Device_Library/Class/dfu/src/usbd_dfu_core.c \
#Libraries/STM32_USB_Device_Library/Class/dfu/src/usbd_dfu_mal.c \
#Libraries/STM32_USB_Device_Library/Class/dfu/src/usbd_flash_if.c \
#Libraries/STM32_USB_Device_Library/Class/dfu/src/usbd_mem_if_template.c \
#Libraries/STM32_USB_Device_Library/Class/dfu/src/usbd_otp_if.c \
#Libraries/STM32_USB_Device_Library/Class/hid/src/usbd_hid_core.c \
#Libraries/STM32_USB_Device_Library/Class/msc/src/usbd_msc_bot.c \
#Libraries/STM32_USB_Device_Library/Class/msc/src/usbd_msc_core.c \
#Libraries/STM32_USB_Device_Library/Class/msc/src/usbd_msc_data.c \
#Libraries/STM32_USB_Device_Library/Class/msc/src/usbd_msc_scsi.c \
#Libraries/STM32_USB_Device_Library/Class/msc/src/usbd_storage_template.c
#Libraries/STM32_USB_Device_Library/Core/src/usbd_core.c \
#Libraries/STM32_USB_Device_Library/Core/src/usbd_ioreq.c \
#Libraries/STM32_USB_Device_Library/Core/src/usbd_req.c \
#Libraries/STM32_USB_HOST_Library/Class/HID/src/usbh_hid_core.c \
#Libraries/STM32_USB_HOST_Library/Class/HID/src/usbh_hid_keybd.c \
#Libraries/STM32_USB_HOST_Library/Class/HID/src/usbh_hid_mouse.c \
#Libraries/STM32_USB_HOST_Library/Class/MSC/src/usbh_msc_bot.c \
#Libraries/STM32_USB_HOST_Library/Class/MSC/src/usbh_msc_core.c \
#Libraries/STM32_USB_HOST_Library/Class/MSC/src/usbh_msc_fatfs.c \
#Libraries/STM32_USB_HOST_Library/Class/MSC/src/usbh_msc_scsi.c \
#Libraries/STM32_USB_HOST_Library/Core/src/usbh_core.c \
#Libraries/STM32_USB_HOST_Library/Core/src/usbh_hcs.c \
#Libraries/STM32_USB_HOST_Library/Core/src/usbh_ioreq.c \
#Libraries/STM32_USB_HOST_Library/Core/src/usbh_stdreq.c \
#Libraries/STM32_USB_OTG_Driver/src/usb_bsp_template.c \
#Libraries/STM32_USB_OTG_Driver/src/usb_core.c \
#Libraries/STM32_USB_OTG_Driver/src/usb_dcd.c \
#Libraries/STM32_USB_OTG_Driver/src/usb_dcd_int.c \
#Libraries/STM32_USB_OTG_Driver/src/usb_hcd.c \
#Libraries/STM32_USB_OTG_Driver/src/usb_hcd_int.c \
#Libraries/STM32_USB_OTG_Driver/src/usb_otg.c \

SRCS += \
Libraries/STM32F4xx_StdPeriph_Driver/src/misc.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_adc.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_can.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_crc.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_cryp.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_cryp_aes.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_cryp_des.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_cryp_tdes.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_dac.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_dbgmcu.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_dcmi.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_dma.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_dma2d.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_exti.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_flash.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_gpio.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_hash.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_hash_md5.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_hash_sha1.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_i2c.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_iwdg.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_ltdc.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_pwr.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_rcc.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_rng.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_rtc.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_sai.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_sdio.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_spi.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_syscfg.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_tim.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_usart.c \
Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_wwdg.c

# Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_fmc.c \
# Libraries/STM32F4xx_StdPeriph_Driver/src/stm32f4xx_fsmc.c \


OBJS = $(SRCS:.c=.o)
DEPS = $(SRCS:.c=.d)

.PHONY: all clean

all: libstm32f4.a

-include $(DEPS)

dirs:
	mkdir -p deps objs
	touch dirs

objs/%.o : %.c dirs
	$(CC) $(CFLAGS) -c -o $@ $< -MMD -MF deps/$(*F).d

libstm32f4.a: $(OBJS)
	$(AR) -r $@ $(OBJS)

clean:
	rm -f dirs $(OBJS) $(DEPS) libstm32f4.a

