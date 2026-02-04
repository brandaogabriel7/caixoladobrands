---
{"dg-publish":true,"dg-path":"Tecnologia/Por que aplicações CPU-bound podem ter a performance prejudicada no Python.md","permalink":"/tecnologia/por-que-aplicacoes-cpu-bound-podem-ter-a-performance-prejudicada-no-python/","tags":["fleeting"],"created":"2024-03-07T15:07:57.737-03:00","updated":"2026-01-23T14:24:41.571-03:00"}
---

Uma aplicação é considerada **CPU-bound** quando seu tempo de resposta depende majoritariamente de operações que utilizam muito poder de processamento da CPU. Esse tipo de aplicação frequentemente pode ser otimizado por meio de concorrência e paralelismo. Basta quebrar os processos em tarefas menores que podem ser executadas em threads diferentes. No entanto, isso não é possível no Python.

Na implementação padrão de Python, existe um *mutex* que só permite que uma thread esteja em execução por vez, o GIL. O **GIL** *(Global Interpreter Lock)* foi criado como uma solução para evitar problemas de concorrência entre as threads, devido à forma como o [[Como funciona o gerenciamento de memória no Python\|Python gerencia a memória]].

O impacto do GIL em aplicações I/O-bound não costuma ser tão grande, visto que as threads em execução podem ser alternadas nos momentos de espera por uma ação de entrada. Já no caso das aplicações CPU-bound, o overhead para utilizar várias threads deixa aplicação menos performática do que se só usasse uma thread.

Deve-se, então, ter atenção para o uso do Python em aplicações CPU-bound. Para contornar a questão do impacto do *GIL* nessas aplicações, pode-se optar pelo uso de outras implementações que não sejam a padrão, ou pelo uso de multiprocessing.
## Referências
- [[Ajitsaria -- What Is the Python Global Interpreter Lock (GIL) - Highlights\|What Is the Python Global Interpreter Lock (GIL)?]]
- [[S -- Exploring Multithreading Concurrency and Parallel Execution in Python - Highlights\|Exploring Multithreading: Concurrency and Parallel Execution in Python]]