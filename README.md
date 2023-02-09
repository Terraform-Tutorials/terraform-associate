# Conceitos importantes sobre o Terraform

## Reference
```txt
Breakdown by content area:

1.0  Understand infrastructure as code (IaC) concepts: 0%
2.0  Understand Terraform's purpose (vs other IaC): 50%
3.0  Understand Terraform basics: 57%
4.0  Use the Terraform CLI (outside of core workflow): 50%
5.0  Interact with Terraform modules: 50%
6.0  Navigate Terraform workflow: 83%
7.0  Implement and maintain state: 37%
8.0  Read, generate, and modify configuration: 63%
9.0  Understand Terraform Cloud and Enterprise capabilities: 100%
```

## IaC Concepts
Então, como o IaC se encaixa no ciclo de vida da infraestrutura? A IaC pode ser aplicada durante todo o ciclo de vida, tanto na construção inicial quanto durante toda a vida útil da infraestrutura. Normalmente, essas atividades são chamadas de atividades do dia 0 e do dia 1. O código “Dia 0” provisiona e configura sua infraestrutura inicial.

Aqui está um exemplo de código que a ferramenta IaC Terraform usaria para provisionar um Amazon VPC. Observe que o código é legível por humanos e máquinas.

```hcl
resource "aws_vpc" "default" {
  cidr_block = "10.0.0.0/16"
}
```

## Meta-Arguments
- `depends_on` - dependencia explicita dentro do terraform.
- `count` - usado para criar numeros de varios recursos, usado em casos quando o objeto e identico.
- `for_each` - similar ao `count` mas para uso em casos quando o objeto de infraestrutura se difere.
- `provider`
- `lifecycle`

## Terraform State File
