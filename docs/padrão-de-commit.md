# Padrão de commit

## Regras

- As mensagens de commit são escritas em **inglês**.
- Todo commit começa com um dos dois prefixos, **entre parênteses**: `(feat)` ou `(fix)`. Nenhum outro é usado.
- **Sem `Co-Authored-By`** nem outras linhas de coautoria.

## Prefixos

| Prefixo  | Quando usar |
|----------|-------------|
| `(feat)` | Algo novo ou alterado: funcionalidade, documentação, estrutura do projeto. |
| `(fix)`  | Correção de erro, seja no código ou em texto/documentação. |

## Formato

```
(<feat|fix>) <short description in english>
```

A descrição fica no imperativo e em minúsculas, sem ponto final.

## Exemplos

```
(feat) add study recommendations module to README
(feat) add commit convention docs
(fix) correct prerequisite chain in curriculum map
(fix) typo in requirements table
```
