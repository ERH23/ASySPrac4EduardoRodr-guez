% Definición de la señal x[n] con duración finita
n = -4:6; % Definición del rango de la señal
x = [1 2 3]; % Valores de la señal para los índices definidos en 'n'

% Función para calcular la energía de x[n]
function energia = calcular_energia(x)
    energia = sum(abs(x).^2); % Suma de los cuadrados de los elementos de x
end

% Función para calcular la potencia de x[n]
function potencia = calcular_potencia(x)
    N = length(x); % Longitud de la señal x
    energia = calcular_energia(x); % Calcular la energía de x
    potencia = energia / N; % Potencia = Energía / N, donde N es el número de muestras
end

% Ejemplo de uso de las funciones
energia_x = calcular_energia(x);
potencia_x = calcular_potencia(x);

disp(['Energía de x[n]: ', num2str(energia_x)]);
disp(['Potencia de x[n]: ', num2str(potencia_x)]);





