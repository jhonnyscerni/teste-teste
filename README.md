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