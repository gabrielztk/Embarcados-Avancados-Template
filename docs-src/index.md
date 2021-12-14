# Coloque aqui o nome do tutorial de vocês

- **Alunos:** Beatriz Muniz / Gabriel Kawall / Rafael dos Santos
- **Curso:** Engenharia da Computação
- **Semestre:** 6 / 8 / 8
- **Contato:** corsiferrao@gmail.com
- **Ano:** 2021

## Começando

Para seguir esse tutorial é necessário:

- **Hardware:** DE10-Standard e acessórios
- **Softwares:** Quartus 18.01
- **Documentos:** [DE10-Standard_User_manual.pdf](https://github.com/Insper/DE10-Standard-v.1.3.0-SystemCD/tree/master/Manual)

## Começando
* Hardware: DE10-Standard
* Softwares: Quartus 18.01


## Motivação
Softwares livres e de código aberto (free and open source ou FOSS do inglês) são um parte essencial da infraestrutura digital do mundo moderno. Existe uma grande diversidade de projetos deste tipo, com escopos e objetivos singelos ou arrojados e mantenedores que vão de indivíduos ou pequenos grupos até empresas multinacionais, ou até mesmo grupos delas. Contudo, quando se trata de hardware existem poucos projetos maduros. Por isso a motivação desse tutorial foi explorar a arquiterura do processador RISC-V, que é uma arquitetura aberta.

A motivação desse tutorial foi explorar a arquiterura  nossa foi bem simples, a arquitetura RISC-V vem crescendo muito rápido e ainda por cima é open-source. Sem contar que ela possui um futuro promissor onde acreditamos que será uma das grandes arquiteturas do futuro.

## Risc-V
Como não é nosso objetivo desenvolver um RISC-V, precisamos clonar o [Risc-V](https://github.com/stnolting/neorv32)


## Hello World
* Criar um projeto no Quartus usando o [neorv32_test_setup_bootloader.vhd](https://github.com/stnolting/neorv32/blob/master/rtl/test_setups/neorv32_test_setup_bootloader.vhd)
* Adcionar todos os arquivos do [rtl/core](https://github.com/stnolting/neorv32/tree/master/rtl/core) no projeto
* Trocar a CLOCK_FREQUENCY para 50 MHz (50e6) no generic


### Pin Map
clk_i : mapear para PIN_AF14
rstn_i : mapear para 
gpio_o : mapear para PIN_AA24, PIN_AB23, PIN_AC23, PIN_AD24, PIN_AG25, PIN_AF25, PIN_AE24, PIN_AF24 (são os pinos dos leds, em vez do gpio)


### Colocando na placa
* Compilar o projeto
* Programar na placa, padraozao mesmo
* ??????
* Profit

### Esta pronto o sorvetinho
Agora o led0 deve estar piscando

## Agora fazendo para rodar um programa C

### Toolchain
Como essse projeto vai utilizar uma arquitetura RISC-V, não podemos utilizar um compilador para outras arquiteturas, logo precisamos baixar um novo compilador/toolchain para o RISC-V.
* Baixar a [release](https://github.com/stnolting/riscv-gcc-prebuilt/releases) da toolchain mais rescente.
* Seguir o [tutorial](https://github.com/stnolting/riscv-gcc-prebuilt/blob/main/README.md) de instalação.

### Compilando
