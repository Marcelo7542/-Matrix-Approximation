Matrix-Approximation of images

English description below

Descrição do Processo

Neste projeto, realizei uma análise de uma imagem usando técnicas de decomposição matricial e quantização de cores. 
O objetivo foi para fins educativos e curiosidade, mostrando como simplificar uma imagem mantendo suas características essenciais. 

Aqui está o processo passo a passo:

Carregamento da Imagem: 

Primeiramente, carrego a imagem de uma paisagem chamada "china.jpg", que é uma imagem de exemplo fornecida pelo scikit-learn. A imagem é carregada e exibida na tela.

Normalização da Imagem: 

Para facilitar o processamento, converto os valores de cor da imagem de inteiros para ponto flutuante e os normalizo para o intervalo de [0, 1], dividindo os valores por 255.

Decomposição SVD (Singular Value Decomposition): 

A partir da imagem normalizada, eu realizo uma decomposição SVD. A SVD decompõe a matriz da imagem em três componentes principais: 

U, sigma e Vt. Cada uma dessas componentes representa diferentes aspectos da informação da imagem, e o objetivo é reconstruir a imagem a partir de um número reduzido de componentes.

Reconstrução da Imagem com Diferentes Ranks: 

Utilizando a decomposição SVD, recrio a imagem com diferentes números de componentes:

Rank-1: Usando apenas o primeiro componente.

Rank-2: Usando os dois primeiros componentes.

Rank-3: Usando os três primeiros componentes.

Cada uma dessas aproximações resulta em uma versão "simplificada" da imagem original, com menos informações preservadas.

Exibição das Aproximações: 

As imagens reconstruídas são exibidas lado a lado, permitindo uma comparação visual do impacto de cada rank na qualidade da imagem.

A imagem original é exibida ao lado das versões com menor rank para observar como a qualidade se degrade à medida que reduzimos o número de componentes.

Cálculo do Erro: 

Calculo o erro associado às aproximações de rank 1 e rank 2. Esse erro é dado pelos valores das componentes não usadas na reconstrução, 
o que nos dá uma ideia da perda de informação ao reduzir o rank.

Quantização de Cores com K-Means: 

Como etapa adicional, realizei a quantização de cores da imagem utilizando o algoritmo de clustering K-Means. 
O K-Means é aplicado para reduzir o número de cores na imagem. A imagem é primeiramente amostrada para selecionar um subconjunto de pixels e, 
em seguida, o algoritmo é treinado para identificar um número específico de cores dominantes.

Reconstrução da Imagem com Cores Quantizadas: 

Após o treinamento do modelo K-Means, cada pixel da imagem é substituído pela cor dominante mais próxima. 
O número de cores pode ser ajustado, e neste caso, defini 100 cores para a quantização.

Exibição da Imagem Quantizada: 

Finalmente, a imagem quantizada é exibida junto com a imagem original. A quantização de cores simplifica a imagem, 
utilizando uma paleta de cores reduzida, mas ainda mantendo a estrutura geral e a aparência visual.

Objetivo

O objetivo foi para fins educativos e curiosidade, 
mostrando como técnicas de redução de dimensionalidade e clustering podem ser aplicadas a imagens para simplificá-las sem perder suas características essenciais. 


Resultados

A imagem original foi comparada com versões simplificadas usando a decomposição SVD com diferentes ranks.

O erro das aproximações foi calculado, mostrando a perda de qualidade com a redução do número de componentes.

A imagem quantizada foi exibida com 100 cores, reduzindo significativamente a complexidade das cores, mas preservando a essência visual da imagem.






English:

Process Description

In this project, I performed an image analysis using matrix decomposition techniques and color quantization. 
The purpose was for educational and curiosity-driven reasons, demonstrating how to simplify an image while maintaining its essential characteristics.

Here is the step-by-step process:

Image Loading:

First, I load the image of a landscape called "china.jpg", which is a sample image provided by scikit-learn. The image is loaded and displayed on the screen.

Image Normalization:

To facilitate processing, I convert the color values of the image from integers to floating-point numbers and normalize them to the [0, 1] range by dividing the values by 255.

SVD Decomposition (Singular Value Decomposition):

From the normalized image, I perform an SVD decomposition. The SVD decomposes the image matrix into three main components:

U, sigma, and Vt. Each of these components represents different aspects of the image's information, and the goal is to reconstruct the image from a reduced number of components.
Image Reconstruction with Different Ranks:

Using the SVD decomposition, I recreate the image with different numbers of components:

Rank-1: Using only the first component.

Rank-2: Using the first two components.

Rank-3: Using the first three components.

Each of these approximations results in a "simplified" version of the original image, with fewer details preserved.

Displaying the Approximations:

The reconstructed images are displayed side by side, allowing a visual comparison of the impact of each rank on image quality.

The original image is shown alongside the lower-rank versions to observe how the quality degrades as we reduce the number of components.

Error Calculation:

I calculate the error associated with the Rank-1 and Rank-2 approximations. This error is given by the values of the components not used in the reconstruction, which provides insight into the loss of information when reducing the rank.

Color Quantization with K-Means:

As an additional step, I performed color quantization on the image using the K-Means clustering algorithm. K-Means is applied to reduce the number of colors in the image. The image is first sampled to select a subset of pixels, and then the algorithm is trained to identify a specific number of dominant colors.

Reconstructing the Image with Quantized Colors:

After training the K-Means model, each pixel in the image is replaced by the nearest dominant color. The number of colors can be adjusted, and in this case, I set 100 colors for the quantization.

Displaying the Quantized Image:

Finally, the quantized image is displayed alongside the original image. Color quantization simplifies the image by using a reduced color palette, while still preserving the overall structure and visual appearance.

Objective
The objective was for educational and curiosity-driven purposes, showing how dimensionality reduction and clustering techniques can be applied to images to simplify them without losing their essential characteristics.

Results

The original image was compared with simplified versions using SVD decomposition with different ranks.

The error of the approximations was calculated, showing the loss of quality as the number of components was reduced.

The quantized image was displayed with 100 colors, significantly reducing the complexity of the colors while preserving the visual essence of the image.
