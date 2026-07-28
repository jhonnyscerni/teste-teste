1. infra/variables.tf (adicionar no fim)

hcl
variable "parameter_ft_limite_flexivel" {
  description = "Chave de valor para habilitar/desabilitar a funcionalidade de Limite Flexivel"
  type        = bool
  default     = false
}

variable "parameter_ft_canal_limite_flexivel" {
  description = "Chave para definir os canais elegiveis para o Limite Flexivel"
  type        = string
  default     = "nenhum"
}

variable "parameter_ft_balde_limite_flexivel" {
  description = "Chave para definir os baldes elegiveis para aplicacao da mutation do Limite Flexivel"
  type        = string
  default     = "nenhum"
}

variable "parameter_ft_segmento_limite_flexivel" {
  description = "Chave para definir os segmentos elegiveis para o Limite Flexivel"
  type        = string
  default     = "nenhum"
}

variable "parameter_ft_dac_limite_flexivel" {
  description = "Chave para definir os DACs de conta elegiveis para o Limite Flexivel"
  type        = string
  default     = "nenhum"
}

2. infra/main.tf — em local_lo5_parameters:

hcl
    FT_limite_flexivel          = var.parameter_ft_limite_flexivel
    FT_canal_limite_flexivel    = var.parameter_ft_canal_limite_flexivel
    FT_balde_limite_flexivel    = var.parameter_ft_balde_limite_flexivel
    FT_segmento_limite_flexivel = var.parameter_ft_segmento_limite_flexivel
    FT_dac_limite_flexivel      = var.parameter_ft_dac_limite_flexivel

E em local_lo5_descriptions:

hcl
    FT_limite_flexivel          = "Feature toggle para ativar/desativar a funcionalidade de Limite Flexivel."
    FT_canal_limite_flexivel    = "Parametro para definir quais canais poderao utilizar o Limite Flexivel."
    FT_balde_limite_flexivel    = "Parametro para definir os baldes elegiveis para aplicacao da mutation."
    FT_segmento_limite_flexivel = "Parametro para definir quais segmentos poderao participar do Limite Flexivel."
    FT_dac_limite_flexivel      = "Parametro para definir os DACs de conta elegiveis para pilotos e rollouts graduais."

3. infra/inventories/dev/terraform.tfvars e hom/terraform.tfvars (idênticos):

hcl
#####################################
## Feature Toggle Limite Flexivel  ##
#####################################
parameter_ft_limite_flexivel          = true
parameter_ft_canal_limite_flexivel    = "C1"
parameter_ft_balde_limite_flexivel    = "PIX"
parameter_ft_segmento_limite_flexivel = "4"
parameter_ft_dac_limite_flexivel      = "4115"

infra/inventories/prod/terraform.tfvars — só a flag principal muda:

hcl
#####################################
## Feature Toggle Limite Flexivel  ##
#####################################
parameter_ft_limite_flexivel          = false
parameter_ft_canal_limite_flexivel    = "C1"
parameter_ft_balde_limite_flexivel    = "PIX"
parameter_ft_segmento_limite_flexivel = "4"
parameter_ft_dac_limite_flexivel      = "4115"