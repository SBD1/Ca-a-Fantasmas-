# Modelo Entidade Relacionamento

## ENTIDADES
- Mundo
- Lugar
- Dificuldade
- Coisa ruim
- Diálogo
- Personagem
- PC
- NPC
- Equipamento
- Fase

## ATRIBUTOS
- Mundo:
  - `<u>id_mundo</u>`
- Lugar:
  - `nome`
  - `descrição`
- Dificuldade:
  - `nível`
- Coisa ruim:
  - `descrição`
  - `consequência`
- Diálogo:
  - `descrição`
- Personagem:
  - `nome`
  - `vida`
  - `características`
- PC:
  - (atributos a serem definidos)
- NPC:
  - `habilidade`
- Equipamento:
  - `nome`
  - `dano`
  - `ataque`
  - `descrição`
- Fase:
  - `numeração`

## RELACIONAMENTOS
### Mundo possui dificuldade:
- Mundo possui uma e apenas uma dificuldade
- Dificuldade é de um e apenas um mundo

### Lugar está no mundo:
- Lugar está em um e apenas um mundo
- Mundo possui no mínimo um e no máximo vários lugares

### PC está no lugar:
- PC pode estar em um e apenas um lugar
- Lugar pode ser ocupado por no mínimo e no máximo um PC

### PC possui equipamento:
- PC possui no mínimo um equipamento e no máximo vários
- Equipamento pode ser de um e apenas um PC

### PC passa fase:
- PC passa nenhuma ou várias fases
- Fase pode ser passada por um e apenas um PC

### PC mata NPC:
- PC mata nenhum ou vários NPC
- NPC mata nenhum ou um PC

### NPC está na fase:
- NPC pertence a uma única fase
- Fase possui apenas um único NPC

### Personagem fala diálogo:
- Personagem fala nenhum ou vários diálogos
- Diálogo pode ser falado por um ou vários personagens

### Lugar possui fase:
- Lugar possui uma ou várias fases
- Fase é de um e apenas um lugar

### Fase possui coisa ruim:
- Fase possui uma coisa ruim
- Coisa ruim pode ser de uma ou várias fases
