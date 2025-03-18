# 2024.2 Avaliação do 1º Período de Sistemas Operacionais  

## Questão 1. Introdução a Sistemas Operacionais  

Os sistemas operacionais gerenciam recursos de hardware e software para garantir eficiência e segurança. Esse gerenciamento envolve:  

### Gerenciamento de Processos  
- O SO controla a execução de processos, garantindo que cada um receba tempo de CPU adequadamente.  
- Exemplo: Em um sistema multitarefa, o SO alterna rapidamente entre processos para que o usuário tenha a sensação de execução simultânea.  

### Gerenciamento de Memória  
- O SO aloca e libera memória para os processos, evitando conflitos e otimizando o uso.  
- Exemplo: Sistemas com memória virtual utilizam parte do disco rígido como extensão da RAM.  

### Gerenciamento de Dispositivos de Entrada e Saída  
- O SO fornece drivers para comunicação com periféricos como teclados, mouses e impressoras.  
- Exemplo: Ao conectar um pendrive, o SO monta automaticamente o dispositivo para acesso aos arquivos.  

### Gerenciamento de Arquivos  
- O SO organiza arquivos em diretórios, controlando permissões e acesso.  
- Exemplo: Em sistemas Unix, usuários podem definir permissões específicas para leitura, escrita e execução de arquivos.  

## Questão 2. Estrutura de Sistemas Operacionais  

As diferentes arquiteturas de sistemas operacionais impactam o custo e a segurança da seguinte forma:  

### Arquitetura Monolítica  
- **Complexidade**: Menor tempo de desenvolvimento inicial, porém manutenção difícil.  
- **Equipe**: Necessita de programadores experientes para evitar falhas que afetem todo o sistema.  
- **Segurança**: Menos segura, pois falhas podem comprometer o SO inteiro.  
- **Exemplo**: O Linux usa um modelo monolítico modularizado.  

### Arquitetura Microkernel  
- **Complexidade**: Desenvolvimento mais lento, mas manutenção mais simples.  
- **Equipe**: Especialização é essencial, pois o sistema é dividido em módulos.  
- **Segurança**: Mais segura, pois serviços críticos são isolados.  
- **Exemplo**: O Minix utiliza essa abordagem.  

### Arquitetura em Camadas  
- **Complexidade**: Desenvolvimento equilibrado, com separação de responsabilidades.  
- **Equipe**: Especialistas podem trabalhar em camadas distintas.  
- **Segurança**: Boa segurança, mas requer controle na comunicação entre camadas.  
- **Exemplo**: O Windows NT utiliza um modelo baseado em camadas.  

## Questão 3. Introdução à Segurança de Sistemas Operacionais  

A implementação de **controles de acesso** e **criptografia** impacta a performance e usabilidade dos sistemas:  

### Benefícios e Desafios  
- **Controles de Acesso** garantem que apenas usuários autorizados acessem recursos, mas podem tornar o sistema mais complexo e difícil de configurar.  
- **Criptografia** protege dados, mas pode impactar o desempenho devido à necessidade de processamento adicional.  

### Impacto na Experiência do Usuário  
- Controles de acesso muito restritivos podem dificultar a usabilidade.  
- Criptografia pode tornar processos como login e transferência de arquivos mais lentos.  

### Exemplos  
- O Windows utiliza o **BitLocker** para criptografar discos inteiros.  
- Sistemas Unix possuem permissões de acesso rigorosas para usuários e grupos.  

## Questão 4. Custo de Processamento vs. Algoritmo Ótimo de Escalonamento  

Os algoritmos de escalonamento afetam o desempenho do SO, e sua escolha depende do custo de processamento.  

### Comparação de Algoritmos  

| Algoritmo  | Vantagens | Desvantagens |
|------------|------------|--------------|
| **FCFS** (First-Come, First-Served) | Simples e justo | Pode causar longos tempos de espera (problema do Convoy Effect) |
| **Round Robin** | Garante que todos os processos tenham tempo de CPU | Pode aumentar a sobrecarga de trocas de contexto |
| **SJN** (Shortest Job Next) | Minimiza tempo médio de espera | Requer conhecimento prévio da duração dos processos |
| **Priority Scheduling** | Permite priorização de processos críticos | Pode levar à inanição de processos de baixa prioridade |

### Impacto na Escolha  
- Sistemas de tempo real exigem algoritmos preditivos, como **SJN** ou **Rate Monotonic Scheduling**.  
- Servidores web podem se beneficiar de **Round Robin** para garantir atendimento a múltiplos usuários.  

## Questão 5. Aplicativo em Python vs. Aplicativos em C  

Os aplicativos em Python e C seguem caminhos distintos até serem executados pelo hardware.  

### Aplicativo em Python  
1. O código-fonte é interpretado pelo **interpretador Python**, linha por linha.  
2. O interpretador converte cada instrução em **bytecode** intermediário.  
3. O bytecode é executado por uma máquina virtual Python (**PVM**).  
4. O **kernel do SO** interage com os drivers de hardware para executar as operações.  

### Aplicativo em C  
1. O código-fonte é **compilado** para código de máquina pelo **compilador C**.  
2. O executável resultante contém instruções binárias prontas para execução direta pelo processador.  
3. O **kernel do SO** gerencia a execução, fornecendo acesso a recursos do hardware.  

### Comparação  
| Característica | Python | C |
|--------------|--------|---|
| **Execução** | Interpretada | Compilada |
| **Velocidade** | Mais lenta | Mais rápida |
| **Portabilidade** | Alta (roda em qualquer SO com Python instalado) | Depende da recompilação para cada SO |
| **Uso do SO** | Depende de uma camada intermediária (PVM) | Comunicação direta com o SO |

### Exemplos  
- Python é utilizado para scripts de automação e aplicações web.  
- C é usado para desenvolvimento de sistemas operacionais e software de alto desempenho.  

---

