# Catálogo de Animes - Funcionalidades de Exportar e Importar JSON

## Funcionalidades Adicionadas

### 📤 Exportar para JSON
- **Botão**: Clique no botão verde "Exportar JSON" no cabeçalho
- **Funcionalidade**: Exporta todo o catálogo atual para um arquivo JSON
- **Arquivo**: O arquivo será baixado com o nome `catalogo-animes-YYYY-MM-DD.json`
- **Conteúdo**: Inclui todos os animes, estatísticas e metadados

### 📥 Importar de JSON
- **Botão**: Clique no botão azul "Importar JSON" no cabeçalho
- **Funcionalidade**: Permite importar dados de um arquivo JSON existente
- **Opções**:
  1. **Substituir Todos**: Remove todos os dados atuais e substitui pelos importados
  2. **Mesclar Dados**: Adiciona novos animes sem remover os existentes

## Como Usar

### Exportando seu Catálogo
1. Clique no botão "Exportar JSON" (verde)
2. O arquivo será baixado automaticamente
3. Guarde este arquivo como backup ou para transferir para outro dispositivo

### Importando um Catálogo
1. Clique no botão "Importar JSON" (azul)
2. Selecione um arquivo JSON válido
3. Escolha uma das opções de importação:
   - **Substituir Todos**: Para restaurar um backup completo
   - **Mesclar Dados**: Para adicionar novos animes ao catálogo existente
4. Confirme a importação

## Formato do Arquivo JSON

O arquivo exportado segue esta estrutura:

```json
{
  "version": "1.0",
  "exportDate": "2024-01-15T10:30:00.000Z",
  "totalAnimes": 3,
  "animes": [
    {
      "id": "unique-id",
      "name": "Nome do Anime",
      "image": "URL da imagem",
      "genres": "Gênero1, Gênero2, Gênero3",
      "status": "watching|completed|plan",
      "totalSeasons": 1,
      "totalEpisodes": 12,
      "watchedEpisodes": 5,
      "startDate": "2024-01-01",
      "endDate": "2024-01-15",
      "externalLinks": ["Link1", "Link2", "Link3"],
      "isFavorite": true,
      "isHidden": false,
      "createdAt": "2024-01-15T10:30:00.000Z",
      "updatedAt": "2024-01-15T10:30:00.000Z"
    }
  ]
}
```

## Casos de Uso

### 🔄 Backup e Restauração
- Exporte seu catálogo regularmente como backup
- Use a opção "Substituir Todos" para restaurar um backup

### 📱 Transferir entre Dispositivos
- Exporte de um dispositivo
- Importe no outro dispositivo usando "Substituir Todos"

### 🤝 Compartilhar Catálogos
- Compartilhe seu arquivo JSON com amigos
- Eles podem usar "Mesclar Dados" para adicionar seus animes favoritos

### 📊 Migração de Dados
- Se você tiver dados em outro formato, converta para JSON
- Importe usando a opção apropriada

## Notas Importantes

- **Backup**: Sempre faça backup antes de importar dados
- **Formato**: Apenas arquivos JSON são aceitos
- **Validação**: O sistema valida o formato do arquivo antes da importação
- **IDs Únicos**: Animes com IDs duplicados não serão importados na opção "Mesclar"
- **Notificações**: O sistema mostra notificações de sucesso/erro para todas as operações

## Arquivo de Exemplo

Incluímos um arquivo `exemplo-catalogo.json` que você pode usar para testar a funcionalidade de importação.

## Suporte

Se encontrar problemas ou tiver dúvidas sobre as funcionalidades de exportar/importar, verifique:
1. Se o arquivo JSON está no formato correto
2. Se não há erros de sintaxe no arquivo
3. Se o arquivo não está corrompido
4. Se o navegador suporta as APIs FileReader e Blob
