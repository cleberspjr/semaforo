## Autor: Cleber Santos Pinto Júnior - https://github.com/cleberspjr


## Temporizador Periódico
Este programa é desenvolvido para rodar em um microcontrolador Raspberry Pi Pico W e controla três LEDs (azul, vermelho e verde) simulando um semáforo 

## Funcionamento do programa
1. Configura os pinos dos LEDs (vermelho, amarelo e verde) como saída.
   Inicializa todos os LEDs apagados e prepara a interrupção do botão.
   O sistema fica em espera, aguardando o pressionamento do botão.

2. Usa add_repeating_timer_ms() para criar um temporizador de 3 segundos.
   A função repeating_timer_callback é chamada a cada 3 segundos para alternar o estado dos LEDs.

3. A variável state controla o estado atual do semáforo (0: vermelho, 1: amarelo, 2: verde).
   A cada chamada do callback, o LED correspondente ao estado atual é aceso, e os outros são apagados.
   O estado é incrementado e reiniciado após o verde (state = (state + 1) % 3).


## MODO DE EXECUÇÃO

1. Clonar o Repositório:

```bash
git clone https: https://github.com/cleberspjr/semaforo
```

2. Configure o ambiente de desenvolvimento seguindo as instruções do Pico SDK

3. Abra o projeto no VS Code

4. Importe o projeto através da extensão Raspberry Pi Tools

5. Execute a simulação através do Wokwi ou da placa Bitdoglab
