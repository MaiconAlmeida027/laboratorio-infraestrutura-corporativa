# CHANGELOG

Histórico de alterações do projeto **Laboratório de Infraestrutura Corporativa**.

O projeto utiliza versionamento incremental para registrar a evolução da infraestrutura, documentação, testes e implementação dos componentes.

---

## [0.1.0] —  Setembro de 2026

### Adicionado

* Criação do projeto de laboratório de infraestrutura corporativa.
* Definição inicial do cenário com matriz e filial.
* Criação da estrutura inicial de diretórios do projeto.
* Criação do `README.md` com objetivo, cenário, arquitetura inicial e roadmap.
* Simulação da infraestrutura de rede utilizando Cisco Packet Tracer.
* Configuração de roteador Cisco 2911.
* Configuração de switch Cisco 2960-24TT.
* Criação da rede da matriz `10.0.0.0/24`.
* Criação da rede da filial `192.168.1.0/24`.
* Configuração de DHCP para a rede da matriz.
* Configuração de DHCP para a rede da filial.
* Configuração dos gateways das duas redes.
* Conexão dos dispositivos da matriz ao switch.
* Comunicação entre matriz e filial através do roteador.
* Realização de testes de conectividade utilizando `ping`.

### Testes realizados

* Validação de obtenção automática de endereço IPv4 via DHCP na matriz.
* Validação de obtenção automática de endereço IPv4 via DHCP na filial.
* Teste de comunicação entre computador da matriz e seu gateway.
* Teste de comunicação entre computador da matriz e computador da filial.
* Confirmação de comunicação entre as redes `10.0.0.0/24` e `192.168.1.0/24`.

### Documentação

* Definição inicial da estrutura de documentação técnica.
* Separação entre requisitos, arquitetura, testes e evidências.
* Definição do processo de evolução do laboratório:

```text
Requisitos
    ↓
Arquitetura
    ↓
Implementação
    ↓
Testes
    ↓
Evidências
    ↓
Documentação
    ↓
Evolução
```

### Próxima etapa

* Documentar formalmente os testes realizados.
* Adicionar evidências dos testes ao projeto.
* Registrar a arquitetura da rede.
* Iniciar a preparação do ambiente virtual para as próximas fases de infraestrutura.
