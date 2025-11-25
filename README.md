# Simulação Segura de Malware --- Projeto Educacional

> **Aviso importante:** este projeto apresenta **apenas simulações
> seguras, pseudocódigo e análises defensivas**. Não contém código que
> execute keylogging no sistema do utilizador, nem ransomware que cifre
> ficheiros reais fora de um ambiente isolado. Qualquer experimento
> prático deve ser feito **somente** em máquinas virtuais isoladas (VM)
> com snapshots e sem ligação à rede de produção.

## Objetivo

Este repositório documenta um estudo prático sobre o funcionamento
conceitual de **ransomware** e **keyloggers**, com foco em:

-   Entendimento do comportamento e vetores de ataque.
-   Simulações seguras (ambiente controlado) e pseudocódigo para fins
    educativos.
-   Estratégias de detecção, prevenção e resposta (defesa).
-   Como apresentar o trabalho como portfólio técnico (GitHub).

## Conteúdo do repositório

-   `README.md` --- este documento.
-   `/docs` --- documentação detalhada (análises, diagrama de
    ataque/defesa).
-   `/simulations` --- **simulações inofensivas** e pseudocódigo (não
    executáveis em host).
-   `/defensive-scripts` --- scripts de análise e detecção.
-   `/images` --- capturas de tela e diagramas (opcional).
-   `/reports` --- relatório final e reflexão sobre contramedidas.

## Orientação de segurança

1.  Use **máquinas virtuais** com snapshot.
2.  Desconecte a VM da rede host.
3.  Trabalhe apenas com ficheiros **artificiais** numa pasta
    `lab_files`.
4.  Não execute scripts em ambientes de produção.

## Simulações seguras

### Ransomware (conceitual)

Fluxo lógico simulado: 1. Listar arquivos em `lab_files`. 2. Criar
**cópias** transformadas (ex.: encode/base64) em `encrypted_copies`. 3.
Criar nota de simulação. 4. Nunca remover ou cifrar arquivos reais.

### Keylogger (conceitual)

Fluxo lógico simulado: 1. Ler arquivo `simulated_input_stream.txt`. 2.
Registrar eventos em `keystroke_log_simulated.txt`. 3. Simular envio
para `outbox_simulated.txt`.

## Scripts defensivos

-   Monitoramento de alterações em massa
-   Heurísticas de detecção
-   Templates de regras YARA
-   Processos com alto I/O

## Reflexão sobre defesa

-   **Prevenção:** backups, segmentação, privilégios mínimos.
-   **Detecção:** EDR, monitoramento de I/O, análise de comportamento.
-   **Resposta:** isolar host, coletar evidências, restaurar backups.
-   **Conscientização:** evitar phishing, política de instalação de
    softwares.

## Como publicar no GitHub

``` bash
git init
git add .
git commit -m "Initial commit — safe malware simulations and defenses"
git remote add origin https://github.com/SEU_USUARIO/SEU_REPO.git
git push -u origin main
```

## Licença e ética

Este repositório é **estritamente educacional** e não deve ser usado
para atividades maliciosas.
