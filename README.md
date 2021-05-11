## Instalacao e configuracao do Freeradius + MySQL e PostgreSQL

Instalação e configuração do ambiente para o funcionamento do Freeradius com integracao com os bancos de dados MySQL e PostgreSQL

#### Sistemas Operacionais suportados

| Serviços   | Versão |
| :------    | ------:|
| Ubuntu     | 18.04.5 LTS   |

#### Dependências

| Serviços   | Versão |
| :------    | ------:|
| ansible     | 2.9.6  |
| sshpass | 1.0.6   |

#### Arquivos de configuracao

> Arquivo de variaveis de configuracao do banco de dados

group_vars/server-freeradius

**database**: escolha do banco de dados (mysql ou postgresql)
**ip_db**: ip do banco de dados
**port_db**: porta do banco de dados
**login_db**: usuario do banco de dados
**password_db**: senha do usuario do banco de dados
**name_db**: nome do banco de dados

> Arquivo de hosts

hosts

[server-freeradius]
**localhost** - IP do servidor freeradius

#### Comando ansible para implantacao

```bash
ansible-playbook freeradius.yml -i hosts --ask-pass
```




