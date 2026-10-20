# Revora — piloto de gestão de falhas

O Revora é um piloto local para transformar registros industriais de falhas em informações úteis para manutenção, engenharia, produção e qualidade.

## Funcionalidades disponíveis no piloto

- Dashboard com indicadores, gráficos por categoria, distribuição por turno e máquinas com mais ocorrências.
- Base fictícia inicial para demonstração.
- Registro manual de ocorrências.
- Filtros por máquina e turno.
- Pesquisa de ocorrências.
- Importação de Excel (.xlsx/.xls) e CSV com mapeamento básico de colunas.
- Exportação dos registros para Excel.
- Configuração visual de campos adicionais no formulário.
- Armazenamento local no navegador usando localStorage.

## Tecnologias

- React + TypeScript + Vite
- Recharts para gráficos
- SheetJS (xlsx) para importação/exportação de planilhas
- Lucide React para ícones
- CSS responsivo

## Executar localmente

Requer Node.js LTS e npm instalados.

```bash
npm install
npm run dev
```

O Vite exibirá o endereço local, normalmente http://localhost:5173.

Para validar a compilação:

```bash
npm run build
npm run preview
```

## Teste de importação

Na tela **Ocorrências**, clique em **Importar planilha** e escolha um arquivo Excel ou CSV. A primeira linha deve conter títulos de colunas. O importador reconhece variações comuns de nomes como Data, Máquina/Equipamento, Turno, Categoria/Tipo de falha, Descrição/Problema, Hora e Tempo de parada.

## Limitações conhecidas desta versão

- Dados guardados em localStorage pertencem ao navegador e ao computador em uso; não existe sincronização entre usuários.
- O sistema ainda não possui autenticação, servidor de API ou banco de dados central.
- Os campos adicionais são exibidos no formulário, mas seus valores ainda não são persistidos.
- A classificação de falhas importadas é simples; categorias desconhecidas são marcadas como “Outras”.
- Indicadores e registros iniciais são fictícios e não devem ser usados para decisões de produção.
- Não é uma versão pronta para produção. Antes de implantação empresarial, implementar backend, PostgreSQL, perfis de acesso, backups, auditoria e testes.

## Próximas etapas sugeridas

1. Validar o fluxo e a interface com usuários.
2. Ajustar o modelo de dados e a importação com planilhas reais anonimizadas.
3. Persistir valores dos campos personalizados.
4. Desenvolver API FastAPI e banco PostgreSQL.
5. Criar importação assistida para mapear colunas desconhecidas.
6. Adicionar login, perfis, trilha de auditoria e backup.
7. Empacotar a instalação local para empresas.

## Nome

**Revora** é o nome provisório do piloto. A disponibilidade de marca e domínio ainda precisa ser verificada antes de uma decisão comercial.