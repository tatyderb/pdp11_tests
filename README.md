# pdp11_tests
Tests for project "Emulator PDP-11" (MIPT)

## Обязательные тесты в рекомендуемом порядке

* 01_sum - сложение чисел 2 и 3.
* 01_sum_mode1 - сложение 2+3 и 1+5 для тех, кто написал костыль и не различает запись в область регистров и память. Проверка записи моды 1.
* 01_sum_neg - сложение чисел 3 + -2
* 02_sob - суммирование массива слов известной длины через sob
* 02_sob_byte - суммирование массива **байт** известной длины через sob
* 02_sob_mode3 - добавим размер массива слов в виде @#N, а не #4
* 03_arr0 - суммирование массива слов неизвестной длины, оканчивающегося нулем.
* 03_arr0_byte - суммирование массива байт неизвестной длины, оканчивающегося нулем.
* 04_mode4 - ожидаемый результат: программа выполняется в цикле и не падает, а останавливается с печатью ошибки.

* 07_putchar - печать одного символа *
* 08_hello - Hello, world! циклом без функций
* 09_mode67 - печать одного символа:    mov R0, odata        ; print *
* 09_mode6_plus - печать одного символа, mov 4(R0), odata    ; print e
* 09_mode6_minus - печать одного символа, mov -2(R0), odata  ; print c
* 10_jsr_rts - Hello, world с функциями.
* 10_jsr_sum - сумма массива слов, оканчивающегося 0 рекурсивной функцией jsr pc, sum
* 10_jsr_sum_r5 - сумма массива слов, оканчивающегося 0 рекурсивной функцией jsr R5, sum (ожидаем r5=21, r4=005234)


## simpe_tests - Простые тесты

* adc - Add Care тест
* ash - ASH
* ashc1 + ashc2 + ashc_odd - ASHC tests - можно без флагов, сложный тест
* asl - ASL, ASLB
* asr - ASR, ASRB
* com - COM, ~src - можно без флагов
* rol - ROL + ROLB, mode 0, 2, 3
* ror - ROR + RORB, mode 0, 2
* div - DIV тест (деление) - можно без флагов
* mul - MUL тест (умножение) - можно без флагов

## zachet - зачетные задачи

* putbin - печать в двоичном виде (с функциями)
* putbin_plane - печать в двоичном виде (без функций)
* putoct - печать в восьмеричном виде (с функциями)
* putoct_plane - печать в восьмеричном виде (без функций)
* puthex - печать в шестнадцатеричном виде (с функциями)
* puthex_plane - печать в шестнадцатеричном виде (без функций)


## Комплексные тесты без печати

* palindrom8 - div - является ли слово восьмеричным палиндромом

## Комплексные тесты с печатью

* 