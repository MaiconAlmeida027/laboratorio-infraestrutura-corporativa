# Laboratório de Infraestrutura Corporativa

Laboratório prático desenvolvido como projeto de estudo para aplicar conceitos de **redes, infraestrutura, administração de sistemas, segurança da informação e documentação técnica**.

O projeto está sendo desenvolvido de forma incremental, partindo da simulação de uma infraestrutura de rede e evoluindo posteriormente para serviços de infraestrutura em máquinas virtuais.

> **Status atual:** Em desenvolvimento — Fase 1: Redes e conectividade.

---

## 🎯 Objetivo

Construir e documentar uma infraestrutura corporativa simulada, utilizando uma abordagem próxima à encontrada em ambientes reais de TI.

O laboratório busca integrar:

* Redes de computadores
* Endereçamento IPv4
* DHCP
* Roteamento
* Administração de sistemas
* Active Directory
* DNS
* GPO e hardening
* Controle de acesso
* Monitoramento
* Gestão de chamados
* Segurança da informação
* Testes e documentação técnica

Os componentes serão implementados progressivamente, conforme o desenvolvimento do laboratório.

---

## 🏢 Cenário

O laboratório representa uma empresa fictícia com uma **matriz** e uma **filial**.

A matriz possui diferentes setores conectados a uma infraestrutura de rede centralizada, enquanto a filial possui sua própria rede e comunicação com a matriz através de um roteador.

### Estrutura inicial

```text
                    ┌─────────────────┐
                    │     ROTEADOR    │
                    │      Cisco      │
                    │      2911       │
                    └────────┬────────┘
                             │
                ┌────────────┴────────────┐
                │                         │
                ▼                         ▼
        REDE DA MATRIZ              REDE DA FILIAL
          10.0.0.0/24               192.168.1.0/24
                │                         │
                ▼                         ▼
        ┌───────────────┐           ┌──────────────┐
        │ Switch Cisco  │           │ Cliente Filial│
        │ 2960-24TT     │           │ NEX-FIL-LOG-01│
        └───────┬───────┘           └──────────────┘
                │
        ┌───────┼────────┬────────┐
        ▼       ▼        ▼        ▼
       RH     FIN       TI       VEN
```

---

## 🌐 Infraestrutura de rede atual

### Matriz

| Item     | Configuração    |
| -------- | --------------- |
| Rede     | `10.0.0.0/24`   |
| Gateway  | `10.0.0.1`      |
| DHCP     | Ativo           |
| Roteador | Cisco 2911      |
| Switch   | Cisco 2960-24TT |

### Filial

| Item     | Configuração     |
| -------- | ---------------- |
| Rede     | `192.168.1.0/24` |
| Gateway  | `192.168.1.1`    |
| DHCP     | Ativo            |
| Roteador | Cisco 2911       |

---

## ✅ Implementado até o momento

### Rede

* [x] Topologia matriz/filial
* [x] Roteador Cisco 2911
* [x] Switch Cisco 2960
* [x] Endereçamento IPv4
* [x] DHCP na matriz
* [x] DHCP na filial
* [x] Gateway configurado
* [x] Comunicação entre redes
* [x] Testes de conectividade com `ping`

### Testes realizados

A comunicação entre um dispositivo da matriz e um dispositivo da filial foi validada através de ICMP.

Exemplo:

```text
Matriz
10.0.0.12

        ↓

Roteador

        ↓

Filial
192.168.1.10
```

Resultado obtido:

```text
Packets: Sent = 4, Received = 4, Lost = 0
```

---

## 🚧 Próximas etapas

A infraestrutura será expandida progressivamente.

### Fase 2 — Infraestrutura de servidores

* [ ] Criar máquinas virtuais
* [ ] Instalar Windows Server
* [ ] Configurar Active Directory
* [ ] Configurar DNS
* [ ] Configurar DHCP em ambiente de servidor
* [ ] Criar usuários e grupos
* [ ] Configurar permissões NTFS
* [ ] Criar políticas de grupo (GPO)

### Fase 3 — Segurança

* [ ] Políticas de senha
* [ ] Princípio do menor privilégio
* [ ] Hardening
* [ ] Restrições de acesso
* [ ] Firewall
* [ ] Auditoria e logs
* [ ] Documentação dos controles de segurança

### Fase 4 — Gestão e monitoramento

Planejamento para integração futura de ferramentas como:

* GLPI
* Zabbix
* Centralização de logs

Esses componentes ainda **não fazem parte da infraestrutura implementada**.

---

## 🧪 Metodologia

O laboratório será desenvolvido seguindo um ciclo incremental:

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

A intenção é documentar não apenas o resultado, mas também as decisões técnicas, problemas encontrados e testes realizados durante o desenvolvimento.

---

## 📁 Estrutura do projeto

```text
laboratorio-infraestrutura-corporativa/
│
├── docs/
│   ├── requisitos/
│   ├── arquitetura/
│   ├── testes/
│   └── evidencias/
│
├── packet-tracer/
│   └── laboratorio.pkt
│
├── virtualbox/
│   └── README.md
│
├── scripts/
│
├── README.md
└── CHANGELOG.md
```

---

## 🛠️ Tecnologias e ferramentas

Atualmente:

* Cisco Packet Tracer
* Cisco IOS
* IPv4
* DHCP
* ICMP
* Git
* GitHub

Planejadas:

* VirtualBox
* Windows Server
* Active Directory
* PowerShell
* DNS
* GPO
* GLPI
* Zabbix

---

## 📚 Contexto acadêmico

O laboratório também será utilizado como projeto prático para consolidar conhecimentos relacionados ao curso de **Análise e Desenvolvimento de Sistemas**, especialmente em áreas como:

* Redes
* Engenharia de Requisitos
* Segurança da Informação
* Sistemas Operacionais
* Banco de Dados
* Administração de sistemas
* Documentação técnica

---

## 📌 Status

**Fase atual:** Redes e conectividade

**Situação:** Em desenvolvimento

O projeto será atualizado conforme novas funcionalidades e componentes forem implementados.
