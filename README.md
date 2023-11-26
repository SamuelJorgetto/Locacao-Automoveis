# Banco de Dados de Locações de Veículos

Este banco de dados é um exemplo simples para o controle de locações de veículos, contendo informações sobre os veículos disponíveis, os clientes e as locações realizadas.

## Estrutura do Banco de Dados

### Tabelas

#### Tabela `veiculos`

A tabela `veiculos` armazena informações sobre as locações de veículos.
- `cod_Locacao`: Chave primária que identifica exclusivamente cada locação.
- `veiculo`: Nome do veículo.
- `cor`: Cor do veículo.
- `placa`: Placa do veículo.
- `diaria`: Valor da diária do veículo.
- `cliente`: Nome do cliente associado à locação.
- `cpf`: CPF do cliente associado à locação.
- `nascimento`: Data de nascimento do cliente.
- `dia`: Número de dias da locação.
- `total`: Valor total da locação.

#### Tabela `cliente`

A tabela `cliente` armazena informações sobre os clientes.
- `cpf`: Chave primária que identifica exclusivamente cada cliente.
- `nome`: Nome do cliente.
- `nascimento`: Data de nascimento do cliente.

#### Tabela `veiculo`

A tabela `veiculo` é uma versão normalizada da tabela `veiculos`.
- `cod_locacao`: Chave primária que identifica exclusivamente cada locação.
- `veiculo`: Nome do veículo.
- `cor`: Cor do veículo.
- `placa`: Placa do veículo.
- `diaria`: Valor da diária do veículo.
- `cpf_cliente`: CPF do cliente associado à locação.
- `dia`: Número de dias da locação.
- `total`: Valor total da locação.
- `cpf_cliente`: Chave estrangeira referenciando a tabela `cliente`.

### Inserção de Dados

Foram inseridos registros de exemplo nas tabelas `cliente` e `veiculo` para demonstrar o funcionamento do banco de dados.

## Consultas e Views

### Consulta de Registros na Tabela `veiculo`

A consulta abaixo exibe os registros presentes na tabela `veiculo`:

```sql
select * from veiculo;
