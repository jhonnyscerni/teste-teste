FT_limite_flexivel          = var.parameter_ft_limite_flexivel
    FT_canal_limite_flexivel    = var.parameter_ft_canal_limite_flexivel
    FT_balde_limite_flexivel    = var.parameter_ft_balde_limite_flexivel
    FT_segmento_limite_flexivel = var.parameter_ft_segmento_limite_flexivel
    FT_dac_limite_flexivel      = var.parameter_ft_dac_limite_flexivel


FT_limite_flexivel          = "Feature toggle para ativar/desativar a funcionalidade de Limite Flexivel."
    FT_canal_limite_flexivel    = "Parametro para definir quais canais poderao utilizar o Limite Flexivel."
    FT_balde_limite_flexivel    = "Parametro para definir os baldes elegiveis para aplicacao da mutation."
    FT_segmento_limite_flexivel = "Parametro para definir quais segmentos poderao participar do Limite Flexivel."
    FT_dac_limite_flexivel      = "Parametro para definir os DACs de conta elegiveis para pilotos e rollouts graduais."



#####################################
## Feature Toggle Limite Flexivel  ##
#####################################
parameter_ft_limite_flexivel          = true
parameter_ft_canal_limite_flexivel    = "C1"
parameter_ft_balde_limite_flexivel    = "PIX"
parameter_ft_segmento_limite_flexivel = "4"
parameter_ft_dac_limite_flexivel      = "4115"