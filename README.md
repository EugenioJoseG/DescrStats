python
def DescrStat(datafile):
    '''
    --------------------------------------------------------------------
    Esta función imprime y retorna estadística descriptiva de un archivo de texto delimitado por comas, de una sola variable
    --------------------------------------------------------------------
    INPUTS:
    datafile = string, path del archivo de datos a usar en la función.
    OTRAS FUNCIONES Y ARCHIVOS LLAMADOS POR ESTA FUNCIÓN: None
    OBJETOS CREADOS EN LA FUNCIÓN:
    data = (N,) vector, data de datafile
    data_mean = scalar, promedio de los datos
    data_std = scalar >= 0, desviación estándar de la data
    data_var = scalar >= 0, varianza de la data
    ARCHIVOS CREADOS PRO ESTA FUNCIÓN: None
    RETURNS: data_mean, data_std, data_var
    --------------------------------------------------------------------
    '''
    data = np.loadtxt(datafile)
    data_mean = data.mean()
    data_std = data.std()
    data_var = data.var()
    print('Promedio de los datos es de:', data_mean)
    print('Desviación Estándar de los datos es de:', data_std)
    print('Varianza de los datos es de:', data_var)
    return data_mean, data_std, data_var
