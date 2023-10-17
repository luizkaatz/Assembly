;Programa hardcore 'completar com nome'
;Introdução ao Assembly
;Author: Luiz Fernando, FEAP
;Version: Luiz Fernando de Almeida Castro Sant'ana, Engenharia da Computação

section .data
    msg db 'A soma é: ',0x0A ; Mensagem a ser exibida com uma quebra de linha
    len equ $ - msg

section .bss
    res resb 1

section .text
    global _start

_start:
    ; Realiza a soma de 3 + 4
    mov eax, 3
    add eax, 4

    ; Converte o resultado em caractere ('0' = 48 em ASCII) e armazena em res
    add eax, '0'
    mov [res], al

    ; Exibe a mensagem
    mov eax, 4
    mov ebx, 1
    mov ecx, msg
    mov edx, len
    int 0x80

    ; Exibe o resultado
    mov eax, 4
    mov ebx, 1
    mov ecx, res
    mov edx, 1
    int 0x80

    ; Sai do programa
    mov eax, 1
    xor ebx, ebx
    int 0x80
