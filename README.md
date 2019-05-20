{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "name": "Python Data Science Libraries.ipynb",
      "version": "0.3.2",
      "provenance": [],
      "collapsed_sections": [
        "MW6qaDctOUxD"
      ]
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "KadEUzaJOKDV",
        "colab_type": "text"
      },
      "source": [
        "#Python Data Science Libraries"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "AK9RUrr19I0O",
        "colab_type": "text"
      },
      "source": [
        "Pandas Cheet Sheet :<br>\n",
        "\n",
        "* https://assets.datacamp.com/blog_assets/PandasPythonForDataScience.pdf\n",
        "*   https://www.kaggle.com/grroverpr/pandas-cheatsheet\n",
        "*  https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Pandas_Cheat_Sheet_2.pdf\n",
        "\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "MW6qaDctOUxD",
        "colab_type": "text"
      },
      "source": [
        "##Dosya İşlemleri"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "JfD69rrgOZ2J",
        "colab_type": "text"
      },
      "source": [
        "### Dosya Okuma\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "zgwjbPxjSbin",
        "colab_type": "text"
      },
      "source": [
        "####open() fonksiyonu"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "RfrVgwcsPExA",
        "colab_type": "text"
      },
      "source": [
        "Dosyayı açmak için open() fonksiyonu kullanılır. FileObject tipi döner.\n",
        "\n",
        "Dosyayı okuma ve yazma olarak iki farklı formatta  açabiliriz. \n",
        "\n",
        "r : okuma  ( dosya yoksa hata verir.)\n",
        "w : yazma ( dosya yoksa oluşturur ve okur)"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "wV-TAQSpQxnz",
        "colab_type": "text"
      },
      "source": [
        "r modundayken **olmayan bir dosya** okumaya çalıştığımızda aşağıdaki hatayı alırız.\n",
        "\n",
        "No such file or directory: 'kisibilgilerim.txt'"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "GgqUzwqPP6IR",
        "colab_type": "code",
        "outputId": "93c4c76a-ef6f-479a-ea00-eb38425b91aa",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 202
        }
      },
      "source": [
        "dosya_adi = \"kisibilgilerim.txt\"\n",
        "myfile = open(dosya_adi, \"r\")"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "error",
          "ename": "FileNotFoundError",
          "evalue": "ignored",
          "traceback": [
            "\u001b[0;31m---------------------------------------------------------------------------\u001b[0m",
            "\u001b[0;31mFileNotFoundError\u001b[0m                         Traceback (most recent call last)",
            "\u001b[0;32m<ipython-input-29-8dee6b4928d5>\u001b[0m in \u001b[0;36m<module>\u001b[0;34m()\u001b[0m\n\u001b[1;32m      1\u001b[0m \u001b[0mdosya_adi\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0;34m\"kisibilgilerim.txt\"\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0;32m----> 2\u001b[0;31m \u001b[0mmyfile\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0mopen\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mdosya_adi\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0;34m\"r\"\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m",
            "\u001b[0;31mFileNotFoundError\u001b[0m: [Errno 2] No such file or directory: 'kisibilgilerim.txt'"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "R-sbj3u1RDYP",
        "colab_type": "text"
      },
      "source": [
        "w modunda olmayan bir dosya okumaya çalıştığımızda oluşturur. "
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "_5HyBMw1RK5d",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "dosya_adi = \"kisibilgileri.txt\"\n",
        "myfile = open(dosya_adi, \"r\")"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "hJMESjecRZKa",
        "colab_type": "text"
      },
      "source": [
        "name özelliği ile dosya adını alırız."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "rUH-9o7ZRYa6",
        "colab_type": "code",
        "outputId": "df17ef31-4c44-4f25-e977-4ebf42d9c1ef",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "myfile.name"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "'kisibilgileri.txt'"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 31
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "XPDQTSu-RwVR",
        "colab_type": "text"
      },
      "source": [
        "mode özelliği ile açılan dosyanın modunu alırız."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "a2OrHaPcR1v-",
        "colab_type": "code",
        "outputId": "fcc94d68-7dc2-496d-f7dc-d2c8f30cb37b",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "myfile.mode"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "'r'"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 32
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "XNsodhq_SDIQ",
        "colab_type": "text"
      },
      "source": [
        "####read() metodu"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "xEQ-RMfPSLov",
        "colab_type": "text"
      },
      "source": [
        "read() fonksiyonu ile tüm dosya içeriği okunur. okunması için r modunda açılması gerekir."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "vFphOl4gSol6",
        "colab_type": "code",
        "outputId": "44abdb27-c94a-4853-ed44-6012a27d81c2",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "dosya_icerigi = myfile.read()\n",
        "dosya_icerigi"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "''"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 33
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "nEhEm-N0T1Ar",
        "colab_type": "text"
      },
      "source": [
        "####close() metodu"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "nyTB_kvKUISH",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "myfile.close()"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "qgjL_vm7U2VA",
        "colab_type": "text"
      },
      "source": [
        "####with ifadesi"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "6uL7jsCoU6t1",
        "colab_type": "text"
      },
      "source": [
        "with ifadesi ile dosyayı açtığımızda otomatik olarak dosya işlem bitince kapatılır. Böylece close() methodunu bizim çağırmamıza gerek kalmaz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "P8i5_wVgU6AE",
        "colab_type": "code",
        "outputId": "505b0102-c98c-4707-bd3b-ceda519d6158",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "with open(dosya_adi,\"r\") as myfile:\n",
        "  dosya_icerigi = myfile.read()\n",
        "  print(dosya_icerigi)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "E6qGhQP0V8hA",
        "colab_type": "text"
      },
      "source": [
        "closed özelliğini çağırarak dosyanın kaptılıp kapatılmadığını görelim."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "JqTMz3mkWHHV",
        "colab_type": "code",
        "outputId": "edc055f0-4528-4970-d60f-8dbff6653ba7",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "myfile.closed"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "True"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 40
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "tumlbIy3WU25",
        "colab_type": "text"
      },
      "source": [
        "dosya_icerigi değişkenine with bloğundan çıktıktan sonra da erişebiliriz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "uMDFTSOqWce6",
        "colab_type": "code",
        "outputId": "57ac9434-234b-4f8b-a843-0d56130e66dd",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "print(dosya_icerigi)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "0MUaKQV1Xeoh",
        "colab_type": "text"
      },
      "source": [
        "dosyaya veri okuma işlemlerini görmek için aşağıdaki gibi elle yazı yazalım.\n",
        "\n",
        "Mehmet Aca <br>\n",
        "Hasibe Zafer <br>\n",
        "Ufuk Türkoğlu <br>"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "bVlQJm10YeOL",
        "colab_type": "code",
        "outputId": "fcf9b14b-ce8b-474d-bcf4-90f3e479f19a",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "dosya_adi =\"kisibilgileri.txt\"\n",
        "with open(dosya_adi,\"r\") as myfile:\n",
        "  dosya_icerigi= myfile.read()\n",
        "  \n",
        "print(dosya_icerigi)  "
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Mehmet Aca \n",
            "Hasibe Zafer \n",
            "Ufuk Türkoğlu\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "e72zre-hZKzT",
        "colab_type": "text"
      },
      "source": [
        "read() metoduna parametre verilirse, parametrenin değeri kadar karakter okuyup imleci orada bekletir. "
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "BaENs0HkZlYr",
        "colab_type": "code",
        "outputId": "7951b1ac-eadf-490f-a319-6a1c77d25c1a",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "dosya_adi =\"kisibilgileri.txt\"\n",
        "\n",
        "with open(dosya_adi,\"r\") as myfile:\n",
        "   \n",
        "  print(myfile.read(8))\n",
        "  print(myfile.read(2))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Mehmet A\n",
            "ca\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "EbVJwCzbahnn",
        "colab_type": "text"
      },
      "source": [
        "####readline() metodu"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "ySjjSvvRaelN",
        "colab_type": "code",
        "outputId": "85f1f915-5386-45a5-890a-13290140e795",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "dosya_adi =\"kisibilgileri.txt\"\n",
        "\n",
        "with open(dosya_adi,\"r\") as myfile:\n",
        "  satir1 = myfile.readline()\n",
        "\n",
        "print(satir1)  "
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Mehmet Aca \n",
            "\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "RUprlcApdpB1",
        "colab_type": "text"
      },
      "source": [
        "for döngüsü ile tüm satırları okuyabiliriz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "p_6uE8NSd4NT",
        "colab_type": "code",
        "outputId": "fc817425-f1fd-4401-cda6-828a5a4e90c6",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 103
        }
      },
      "source": [
        "dosya_adi =\"kisibilgileri.txt\"\n",
        "\n",
        "with open(dosya_adi,\"r\") as myfile:\n",
        "  \n",
        "  for satir in myfile:\n",
        "    print(satir)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Mehmet Aca \n",
            "\n",
            "Hasibe Zafer \n",
            "\n",
            "Ufuk Türkoğlu\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "hMxkZ5fafSUZ",
        "colab_type": "text"
      },
      "source": [
        "#### readlines() metodu"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "VrZj9ZhifVfK",
        "colab_type": "text"
      },
      "source": [
        "Tüm satırları okuyup list olarak döner."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "FICrP1n2fbLw",
        "colab_type": "code",
        "outputId": "37ef513f-efce-4c93-97a8-a13fdb99618c",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "dosya_adi =\"kisibilgileri.txt\"\n",
        "\n",
        "with open(dosya_adi,\"r\") as myfile:\n",
        "  satir_listesi = myfile.readlines()\n",
        "  \n",
        "\n",
        "print(len(satir_listesi))\n",
        "print(satir_listesi[1])"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "3\n",
            "Hasibe Zafer \n",
            "\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "jXdXRB43Obma",
        "colab_type": "text"
      },
      "source": [
        "###Dosya Yazma"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "QTpyqcnVjCRm",
        "colab_type": "text"
      },
      "source": [
        "#### write() metodu"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "r0aPX6TkjHQc",
        "colab_type": "text"
      },
      "source": [
        "dosyaya yazmak için w modunda write metodu kullanılır. Dosyanın içinde veri varsa üzerine yazar. yazdıktan sonra alt satıra geçer."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "7CuzQ1s6jOrS",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "dosya_adi =\"kisibilgileri.txt\"\n",
        "\n",
        "with open(dosya_adi,\"w\") as myfile:\n",
        "  myfile.write(\"Mehmet Aca\")\n",
        "  "
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "sZziFVtZjuvD",
        "colab_type": "text"
      },
      "source": [
        "dosyayı okuyup yazdığını görelim."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "u_5w3_UUjyek",
        "colab_type": "code",
        "outputId": "53da3d98-cc68-4a16-a03e-64fb7a54ef05",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "dosya_adi = \"kisibilgileri.txt\"\n",
        "\n",
        "with open(dosya_adi,\"r\") as myfile:\n",
        "  dosya_icerigi = myfile.read()\n",
        "\n",
        "print(dosya_icerigi)  "
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Mehmet Aca\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "ZXNxhDVWlEvB",
        "colab_type": "text"
      },
      "source": [
        "Birden fazla satır yazmak için write() metodunu birden fazla çağırırız. alt satırna inmesi için \\n ekleriz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "DKHOAPwmlXm0",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "dosya_adi =\"kisibilgileri.txt\"\n",
        "\n",
        "with open(dosya_adi,\"w\") as myfile:\n",
        "  myfile.write(\"Mehmet Aca\\n\")\n",
        "  myfile.write(\"Hasibe Zafer\\n\")\n",
        "  myfile.write(\"Erdem Günay\\nUfuk Türkoğlu\\n\")\n",
        "  "
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "4SZQKKQWllu3",
        "colab_type": "text"
      },
      "source": [
        "yazdıklarımızı okuyalım."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "0L45fhAaln_6",
        "colab_type": "code",
        "outputId": "3435c09c-085d-4a9b-fc70-22769ad14c83",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 103
        }
      },
      "source": [
        "dosya_adi = \"kisibilgileri.txt\"\n",
        "\n",
        "with open(dosya_adi,\"r\") as myfile:\n",
        "  dosya_icerigi = myfile.read()\n",
        "\n",
        "print(dosya_icerigi)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Mehmet Aca\n",
            "Hasibe Zafer\n",
            "Erdem Günay\n",
            "Ufuk Türkoğlu\n",
            "\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "9zsLmNqTmfGK",
        "colab_type": "text"
      },
      "source": [
        "#### \"a\" modu"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "fwSJkCVymnL1",
        "colab_type": "text"
      },
      "source": [
        "dosyaya önceki verilerin sonuna veri eklemek için \"a\" modu kullanılır."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "rT1gLvs_mvs9",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "dosya_adi = \"kisibilgileri.txt\"\n",
        "\n",
        "with open(dosya_adi,\"a\") as myfile:\n",
        "  myfile.write(\"bu satır dosyanın sonuna eklenecek.\")"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "T2Ej6lpkm8SH",
        "colab_type": "text"
      },
      "source": [
        "yazdığımızı okuyalım."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "cbrXWpspm_DR",
        "colab_type": "code",
        "outputId": "26414841-fb4c-4606-8a7f-97ef825bf747",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 103
        }
      },
      "source": [
        "dosya_adi = \"kisibilgileri.txt\"\n",
        "\n",
        "with open(dosya_adi,\"r\") as myfile:\n",
        "  dosya_icerigi = myfile.read()\n",
        "\n",
        "print(dosya_icerigi)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Mehmet Aca\n",
            "Hasibe Zafer\n",
            "Erdem Günay\n",
            "Ufuk Türkoğlu\n",
            "bu satır dosyanın sonuna eklenecek.\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "_5A5VX-AnfkM",
        "colab_type": "text"
      },
      "source": [
        "####listeyi dosyaya yazma"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "vJvn70xLnpPX",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "meyveler =[\"elma\",\"armut\",\"kiraz\"]\n",
        "\n",
        "dosya_adi = \"meyveler.txt\"\n",
        "\n",
        "with open(dosya_adi,\"w\") as myfile:\n",
        "  \n",
        "  for meyve in meyveler:\n",
        "    myfile.write(meyve)\n"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "owwpzKKvoK6c",
        "colab_type": "text"
      },
      "source": [
        "meyveler.txt dosyası oluşmuş oldu. Şimdi de okuyalım."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "dSvwLjoRnzaG",
        "colab_type": "code",
        "outputId": "6ce5fbc9-dd6d-44dd-95a1-8f4eecdcc6d8",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "dosya_adi =\"meyveler.txt\"\n",
        "with open(dosya_adi,\"r\") as myfile:\n",
        "  dosya_icerigi = myfile.read()\n",
        "\n",
        "print(dosya_icerigi)  "
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "elmaarmutkiraz\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "EoS0ESUzorGP",
        "colab_type": "text"
      },
      "source": [
        "listedeki her bir elemanı ayrı satırlara yazmak için \\n eklenir."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "LS2L_48-oztQ",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "meyveler =[\"elma\",\"armut\",\"kiraz\"]\n",
        "\n",
        "dosya_adi = \"meyveler.txt\"\n",
        "\n",
        "with open(dosya_adi,\"w\") as myfile:\n",
        "  \n",
        "  for meyve in meyveler:\n",
        "    myfile.write(meyve +\"\\n\")"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "4n8X1QqFo3l6",
        "colab_type": "text"
      },
      "source": [
        "okuyalım"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "uqdQz8XXo49z",
        "colab_type": "code",
        "outputId": "3be51d95-6690-41d0-c029-a0ca458bd737",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 86
        }
      },
      "source": [
        "dosya_adi =\"meyveler.txt\"\n",
        "with open(dosya_adi,\"r\") as myfile:\n",
        "  dosya_icerigi = myfile.read()\n",
        "\n",
        "print(dosya_icerigi) "
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "elma\n",
            "armut\n",
            "kiraz\n",
            "\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "7O9QyNry7Rbb",
        "colab_type": "text"
      },
      "source": [
        "#### Dosya İşlemleri Proje"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "InGOWRZO7Ym2",
        "colab_type": "text"
      },
      "source": [
        "a.txt dosyasındaki tekrarlı verileri temizleyerek  b.txt dosyasına tekil olarak yazan örnek."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "bpTjmPc27RBo",
        "colab_type": "code",
        "outputId": "1ab343d8-5058-412b-c9ed-8a0f9d00c8d5",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 88
        }
      },
      "source": [
        "dosya_adi =\"a.txt\"\n",
        "a_list=[]\n",
        "with open(dosya_adi,\"r\") as a_dosyasi:\n",
        "  a_list = a_dosyasi.readlines()\n",
        "\n",
        "print(a_list)\n",
        "\n",
        "for i in range(len(a_list)):\n",
        "  a_list[i] = a_list[i].replace(\"\\n\",\"\")\n",
        "\n",
        "print(a_list)\n",
        "# uniq veri tuttuğu için sete dönüştürüyoruz listeyi.\n",
        "a_uniq = set(a_list)\n",
        "print(a_uniq)\n",
        "\n",
        "\n",
        "yeni_dosya_adi =\"b.txt\"\n",
        "\n",
        "with open(yeni_dosya_adi,\"w\") as b_dosyasi:\n",
        "  for yeni in a_uniq:\n",
        "    b_dosyasi.write(yeni +\"\\n\")\n",
        "    \n",
        "    \n",
        "\n",
        "  "
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "['Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe\\n', 'Mehmet\\n', 'Hasibe']\n",
            "['Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe', 'Mehmet', 'Hasibe']\n",
            "{'Mehmet', 'Hasibe'}\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "8rHH9xoC99wq",
        "colab_type": "text"
      },
      "source": [
        "b dosyasını okuyalım"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "Err8eUPK-Crh",
        "colab_type": "code",
        "outputId": "9001f607-b703-4aea-a726-21c4f4463b73",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "dosya_adi =\"b.txt\"\n",
        "\n",
        "with open(dosya_adi,\"r\") as b_dosyasi:\n",
        "  icerik = b_dosyasi.read()\n",
        "\n",
        "print(icerik)  "
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Mehmet\n",
            "Hasibe\n",
            "\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "GAH0Vy3_B4nT",
        "colab_type": "text"
      },
      "source": [
        "## Pandas"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "bvJTZRBSCnsa",
        "colab_type": "text"
      },
      "source": [
        "Pandas veri analizi için en popüler kütüphanelerden biridir. \n",
        "\n",
        "\n",
        "\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "pbMkYwEPC2Gq",
        "colab_type": "text"
      },
      "source": [
        "### Pandas kütüphanesinin import edilmesi"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "oa1ChU8Z548m",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "import pandas"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "5r3oRSpwruqz",
        "colab_type": "text"
      },
      "source": [
        "İki veri yapısı vardır.\n",
        "\n",
        "> Pandas Series ( Tek boyutlu Dizi)\n",
        "\n",
        "> DataFrame ( İki boyutlu Dizi)\n",
        "\n",
        "\n",
        "\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "23w76nSmsOiS",
        "colab_type": "text"
      },
      "source": [
        "Pandas Series\n",
        "\n",
        "> List'te olduğu gibi farklı veri tiplerini tutabiliyor. \n",
        "\n",
        "> Mutable (değiştirilebilir )\n",
        "\n",
        "> Ordered (index ile erişilebilir. )\n",
        "\n",
        "Normal listten farkı her bir elemana bir label  verilebiliyor. "
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "OCBI3FOjsNzI",
        "colab_type": "code",
        "outputId": "2713b867-bbeb-4205-d718-ddac10993b42",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series\n",
        "market = pd.Series(data = [], index = [])\n",
        "\n",
        "market"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "Series([], dtype: float64)"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 3
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "YroWpCZFtYQR",
        "colab_type": "code",
        "outputId": "1581a75e-e4f5-4af8-f730-f35c13e41821",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series\n",
        "market = pd.Series(data = [30,6], index = ['yumurta','elma'])\n",
        "\n",
        "market"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "yumurta    30\n",
              "elma        6\n",
              "dtype: int64"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 4
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "LSeMc7l9tux3",
        "colab_type": "text"
      },
      "source": [
        "Açıkça data ve index ifadeleri yazılmadan da kullanılabilir."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "NdxwdVOntpPJ",
        "colab_type": "code",
        "outputId": "4f17ad12-bdcf-4909-b658-4f6cefa2daac",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series\n",
        "market = pd.Series([30,6], ['yumurta','elma'])\n",
        "\n",
        "market"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "yumurta    30\n",
              "elma        6\n",
              "dtype: int64"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 6
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "rQk0fHmisfTD",
        "colab_type": "code",
        "outputId": "2f226fe2-13fe-4dce-99d5-a5ad2addd5b0",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 103
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series market ürünleri\n",
        "market = pd.Series(data = [30, 6, 'Yes', 'No'], index = ['yumurta', 'elma', 'süt', 'ekmek'])\n",
        "\n",
        "market"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "yumurta     30\n",
              "elma         6\n",
              "süt        Yes\n",
              "ekmek       No\n",
              "dtype: object"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 9
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "oI1H4uW2uwq7",
        "colab_type": "code",
        "outputId": "27fbbcd4-e9e6-4fa1-b3d1-8aa020bef347",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series market ürünleri\n",
        "market = pd.Series(data = [30, 6, 'Yes', 'No'], index = ['yumurta', 'elma', 'süt', 'ekmek'])\n",
        "\n",
        "\n",
        "print('veriler:', market.values)\n",
        "print('indexler:', market.index)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "veriler: [30 6 'Yes' 'No']\n",
            "indexler: Index(['yumurta', 'elma', 'süt', 'ekmek'], dtype='object')\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "YR6jjFJfvMFo",
        "colab_type": "text"
      },
      "source": [
        "İstediğimiz veri Seri'de var mı kontrolu"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "_sVHe62JvLWR",
        "colab_type": "code",
        "outputId": "905eb4b1-e153-4981-b58b-17a367e764ae",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series market ürünleri\n",
        "market = pd.Series(data = [30, 6, 'Yes', 'No'], \n",
        "                   index = ['yumurta', 'elma', 'süt', 'ekmek'])\n",
        "\n",
        "'muz' in market"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "False"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 13
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "w9nxJ_T6wCAa",
        "colab_type": "text"
      },
      "source": [
        "bir index'e ait değere ulaşmak için list mantığındaki gibi index ismi veya index verilir."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "miaKkyXTv-lo",
        "colab_type": "code",
        "outputId": "c269bbe4-7a99-48be-9b2b-f3f3beb9487a",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series market ürünleri\n",
        "market = pd.Series(data = [30, 6, 'Yes', 'No'], \n",
        "                   index = ['yumurta', 'elma', 'süt', 'ekmek'])\n",
        "\n",
        "\n",
        "print(market[1])\n",
        "print(market[\"elma\"])\n"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "6\n",
            "6\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "rjbJSZ3rwoU_",
        "colab_type": "text"
      },
      "source": [
        "biden fazla index değerine, index isimlerini veya sırasını liste şeklinde vererek ulaşabiliriz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "wGjsz1-ywtA7",
        "colab_type": "code",
        "outputId": "8576d6e6-7a27-444c-c316-93b25e48f4d9",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series market ürünleri\n",
        "market = pd.Series(data = [30, 6, 'Yes', 'No'], \n",
        "                   index = ['yumurta', 'elma', 'süt', 'ekmek'])\n",
        "\n",
        "\n",
        "print(market[[\"elma\",\"yumurta\"]])"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "elma        6\n",
            "yumurta    30\n",
            "dtype: object\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "1vEf3UJrxcXL",
        "colab_type": "code",
        "outputId": "ed54b7eb-2c5a-45d4-af1a-110b8f9b94ae",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series market ürünleri\n",
        "market = pd.Series(data = [30, 6, 'Yes', 'No'], \n",
        "                   index = ['yumurta', 'elma', 'süt', 'ekmek'])\n",
        "\n",
        "#yumurta, elma\n",
        "print(market[[1,0]])"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "elma        6\n",
            "yumurta    30\n",
            "dtype: object\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "WsWsVnVeyHlY",
        "colab_type": "text"
      },
      "source": [
        "Verilere erişmek için kullanılabilecek metodlar\n",
        "\n",
        "> loc ( laber ismi)\n",
        "\n",
        "> iloc ( label sayısal indexi)\n",
        "\n",
        "\n",
        "\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "FsqOyvTbzkly",
        "colab_type": "text"
      },
      "source": [
        "**loc metodu**"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "3gBOvLAOyV7P",
        "colab_type": "code",
        "outputId": "fe96fcd7-fda4-4085-88a7-167530135bd7",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 120
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series market ürünleri\n",
        "market = pd.Series(data = [30, 6, 'Yes', 'No'], \n",
        "                   index = ['yumurta', 'elma', 'süt', 'ekmek'])\n",
        "print(market.loc[\"yumurta\"])\n",
        "\n",
        "\n",
        "print(\"\\n\")\n",
        "\n",
        "#birden fazla index varsa list şeklinde verilir.\n",
        "\n",
        "print(market.loc[[\"yumurta\",\"elma\"]])"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "30\n",
            "\n",
            "\n",
            "yumurta    30\n",
            "elma        6\n",
            "dtype: object\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "canvrxPtz9Bm",
        "colab_type": "text"
      },
      "source": [
        "**iloc metodu**"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "dCgSKj_I0Fye",
        "colab_type": "code",
        "outputId": "0820843f-aeac-4b55-ce91-221a1d1bf6e0",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 120
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series market ürünleri\n",
        "market = pd.Series(data = [30, 6, 'Yes', 'No'], \n",
        "                   index = ['yumurta', 'elma', 'süt', 'ekmek'])\n",
        "\n",
        "#yumurta\n",
        "print(market.iloc[0])\n",
        "\n",
        "\n",
        "print(\"\\n\")\n",
        "\n",
        "#birden fazla index varsa list şeklinde verilir.\n",
        "#yumurta, elma\n",
        "print(market.iloc[[0,1]])"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "30\n",
            "\n",
            "\n",
            "yumurta    30\n",
            "elma        6\n",
            "dtype: object\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "5BFnaTMP2EaL",
        "colab_type": "text"
      },
      "source": [
        "**Veri güncellemek**"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "bcCzp9_h2Izy",
        "colab_type": "code",
        "outputId": "9503b751-a356-4ed7-8a0c-b4b70bf85890",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 240
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series market ürünleri\n",
        "market = pd.Series(data = [30, 6, 'Yes', 'No'], \n",
        "                   index = ['yumurta', 'elma', 'süt', 'ekmek'])\n",
        "\n",
        "print(market)\n",
        "\n",
        "market[\"ekmek\"] =\"Yes\"\n",
        "\n",
        "print(\"\\n yeni hali \\n\")\n",
        "\n",
        "print(market)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "yumurta     30\n",
            "elma         6\n",
            "süt        Yes\n",
            "ekmek       No\n",
            "dtype: object\n",
            "\n",
            " yeni hali \n",
            "\n",
            "yumurta     30\n",
            "elma         6\n",
            "süt        Yes\n",
            "ekmek      Yes\n",
            "dtype: object\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "-gdZmK0e2tSw",
        "colab_type": "text"
      },
      "source": [
        "**Veri Silmek**"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "nl_LnV4T2wFH",
        "colab_type": "text"
      },
      "source": [
        "drop metodu kullanılır."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "7iy1-BNM3DVS",
        "colab_type": "code",
        "outputId": "d8846914-0768-426b-d350-b14d7152be73",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 343
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "#  Pandas Series market ürünleri\n",
        "market = pd.Series(data = [30, 6, 'Yes', 'No'], \n",
        "                   index = ['yumurta', 'elma', 'süt', 'ekmek'])\n",
        "\n",
        "print(\"Orjinal :\\n\", market)\n",
        "\n",
        "# Bu şekilde Serinin kendisini değiştirmez yeni bir seri verir.\n",
        "market.drop(\"elma\")\n",
        "\n",
        "print(\"\\n elmayı drop ettikten sonra : \\n\", market)\n",
        "\n",
        "\n",
        "# Serinin kendisini değiştirmek istersek\n",
        "market.drop(\"elma\",inplace=True)\n",
        "\n",
        "print(\"\\n inplace parametresinden sonra : \\n\", market)\n",
        "\n"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Orjinal :\n",
            " yumurta     30\n",
            "elma         6\n",
            "süt        Yes\n",
            "ekmek       No\n",
            "dtype: object\n",
            "\n",
            " elmayı drop ettikten sonra : \n",
            " yumurta     30\n",
            "elma         6\n",
            "süt        Yes\n",
            "ekmek       No\n",
            "dtype: object\n",
            "\n",
            " inplace parametresinden sonra : \n",
            " yumurta     30\n",
            "süt        Yes\n",
            "ekmek       No\n",
            "dtype: object\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "QLRbgFnSDH6t",
        "colab_type": "text"
      },
      "source": [
        "### Bir csv dosyasını okumak"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "SrQS_OdDDNH8",
        "colab_type": "code",
        "outputId": "d878ef21-8e5d-4b53-e58f-7f6b126d6450",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 206
        }
      },
      "source": [
        "import pandas\n",
        "\n",
        "csv_path=\"https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%204/Datasets/TopSellingAlbums.csv\"\n",
        "#csv_path = \"file1.csv\"\n",
        "df = pandas.read_csv(csv_path)\n",
        "\n",
        "print(df)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "            Artist                            Album  ...  Soundtrack Rating\n",
            "0  Michael Jackson                         Thriller  ...         NaN   10.0\n",
            "1            AC/DC                    Back in Black  ...         NaN    9.5\n",
            "2       Pink Floyd        The Dark Side of the Moon  ...         NaN    9.0\n",
            "3  Whitney Houston                    The Bodyguard  ...           Y    8.5\n",
            "4        Meat Loaf                  Bat Out of Hell  ...         NaN    8.0\n",
            "5           Eagles  Their Greatest Hits (1971-1975)  ...         NaN    7.5\n",
            "6         Bee Gees             Saturday Night Fever  ...           Y    7.0\n",
            "7    Fleetwood Mac                          Rumours  ...         NaN    6.5\n",
            "\n",
            "[8 rows x 10 columns]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "7r4QiLUoFemT",
        "colab_type": "text"
      },
      "source": [
        "import pandas as pd kullanımı"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "GzeDeLaiFkB6",
        "colab_type": "code",
        "outputId": "99c37667-e84c-46ab-8556-1db16028f05b",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 206
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "csv_path=\"https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%204/Datasets/TopSellingAlbums.csv\"\n",
        "#csv_path = \"file1.csv\"\n",
        "df = pd.read_csv(csv_path)\n",
        "\n",
        "print(df)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "            Artist                            Album  ...  Soundtrack Rating\n",
            "0  Michael Jackson                         Thriller  ...         NaN   10.0\n",
            "1            AC/DC                    Back in Black  ...         NaN    9.5\n",
            "2       Pink Floyd        The Dark Side of the Moon  ...         NaN    9.0\n",
            "3  Whitney Houston                    The Bodyguard  ...           Y    8.5\n",
            "4        Meat Loaf                  Bat Out of Hell  ...         NaN    8.0\n",
            "5           Eagles  Their Greatest Hits (1971-1975)  ...         NaN    7.5\n",
            "6         Bee Gees             Saturday Night Fever  ...           Y    7.0\n",
            "7    Fleetwood Mac                          Rumours  ...         NaN    6.5\n",
            "\n",
            "[8 rows x 10 columns]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "u2ncXRtKFwEf",
        "colab_type": "text"
      },
      "source": [
        "####df.head() metodu"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "MLHNshlyHpYa",
        "colab_type": "text"
      },
      "source": [
        "Tüm sütunları ve ilk 5 satırı döndürür."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "KwsDo_RcF01H",
        "colab_type": "code",
        "outputId": "e423c95c-3335-4f6a-c05d-ddc3bb57504d",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 394
        }
      },
      "source": [
        "import pandas as pd\n",
        "# adresteki dosyayı indirip colaba yükledik.\n",
        "csv_path=\"TopSellingAlbums.csv\"\n",
        "df = pd.read_csv(csv_path)\n",
        "\n",
        "df.head()"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/html": [
              "<div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>Artist</th>\n",
              "      <th>Album</th>\n",
              "      <th>Released</th>\n",
              "      <th>Length</th>\n",
              "      <th>Genre</th>\n",
              "      <th>Music Recording Sales (millions)</th>\n",
              "      <th>Claimed Sales (millions)</th>\n",
              "      <th>Released.1</th>\n",
              "      <th>Soundtrack</th>\n",
              "      <th>Rating</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>0</th>\n",
              "      <td>Michael Jackson</td>\n",
              "      <td>Thriller</td>\n",
              "      <td>1982</td>\n",
              "      <td>0:42:19</td>\n",
              "      <td>pop, rock, R&amp;B</td>\n",
              "      <td>46.0</td>\n",
              "      <td>65</td>\n",
              "      <td>30-Nov-82</td>\n",
              "      <td>NaN</td>\n",
              "      <td>10.0</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>AC/DC</td>\n",
              "      <td>Back in Black</td>\n",
              "      <td>1980</td>\n",
              "      <td>0:42:11</td>\n",
              "      <td>hard rock</td>\n",
              "      <td>26.1</td>\n",
              "      <td>50</td>\n",
              "      <td>25-Jul-80</td>\n",
              "      <td>NaN</td>\n",
              "      <td>9.5</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>2</th>\n",
              "      <td>Pink Floyd</td>\n",
              "      <td>The Dark Side of the Moon</td>\n",
              "      <td>1973</td>\n",
              "      <td>0:42:49</td>\n",
              "      <td>progressive rock</td>\n",
              "      <td>24.2</td>\n",
              "      <td>45</td>\n",
              "      <td>01-Mar-73</td>\n",
              "      <td>NaN</td>\n",
              "      <td>9.0</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>3</th>\n",
              "      <td>Whitney Houston</td>\n",
              "      <td>The Bodyguard</td>\n",
              "      <td>1992</td>\n",
              "      <td>0:57:44</td>\n",
              "      <td>R&amp;B, soul, pop</td>\n",
              "      <td>27.4</td>\n",
              "      <td>44</td>\n",
              "      <td>17-Nov-92</td>\n",
              "      <td>Y</td>\n",
              "      <td>8.5</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>4</th>\n",
              "      <td>Meat Loaf</td>\n",
              "      <td>Bat Out of Hell</td>\n",
              "      <td>1977</td>\n",
              "      <td>0:46:33</td>\n",
              "      <td>hard rock, progressive rock</td>\n",
              "      <td>20.6</td>\n",
              "      <td>43</td>\n",
              "      <td>21-Oct-77</td>\n",
              "      <td>NaN</td>\n",
              "      <td>8.0</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div>"
            ],
            "text/plain": [
              "            Artist                      Album  ...  Soundtrack Rating\n",
              "0  Michael Jackson                   Thriller  ...         NaN   10.0\n",
              "1            AC/DC              Back in Black  ...         NaN    9.5\n",
              "2       Pink Floyd  The Dark Side of the Moon  ...         NaN    9.0\n",
              "3  Whitney Houston              The Bodyguard  ...           Y    8.5\n",
              "4        Meat Loaf            Bat Out of Hell  ...         NaN    8.0\n",
              "\n",
              "[5 rows x 10 columns]"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 119
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "W_7geNT0HyqZ",
        "colab_type": "text"
      },
      "source": [
        "####read_excel() metodu"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "vKDOi9ooH3us",
        "colab_type": "text"
      },
      "source": [
        "Excel dosyalarını okumak için kullanılır."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "VSPZQAHxICcT",
        "colab_type": "code",
        "outputId": "68394998-78da-4511-cf70-6952562ec4b6",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 463
        }
      },
      "source": [
        "import pandas as pd\n",
        "excel_path=\"veribilimi.xlsx\"\n",
        "df = pd.read_excel(excel_path)\n",
        "\n",
        "df.head()"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/html": [
              "<div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>Zaman damgası</th>\n",
              "      <th>E-posta Adresi</th>\n",
              "      <th>Adınız Soyadınız</th>\n",
              "      <th>Telefon Numarası</th>\n",
              "      <th>Python bilgi seviyeniz</th>\n",
              "      <th>Numpy bilgi seviyeniz</th>\n",
              "      <th>Pandas bilgi seviyeniz</th>\n",
              "      <th>Matplotlib bilgi seviyeniz</th>\n",
              "      <th>Öğrenci misiniz ?</th>\n",
              "      <th>Öğrenciyseniz kaçıncı sınıftasınız ?</th>\n",
              "      <th>Öğrenciyseniz okulunuzu/bölümünüzü; çalışıyorsanız şirket/pozisyonunuzu yazınız.</th>\n",
              "      <th>Bu eğitime neden katılmak istiyorsunuz ?</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>0</th>\n",
              "      <td>2019-05-16 05:35:22.919</td>\n",
              "      <td>eseven41@gmail.com</td>\n",
              "      <td>Engin seven</td>\n",
              "      <td>1. Seçenek</td>\n",
              "      <td>Başlangıç Seviyesi</td>\n",
              "      <td>Hiç bilmiyorum</td>\n",
              "      <td>Hiç bilmiyorum</td>\n",
              "      <td>Hiç bilmiyorum</td>\n",
              "      <td>Hayır</td>\n",
              "      <td>NaN</td>\n",
              "      <td>Milli Eğitim bakanlığı</td>\n",
              "      <td>Python öğrenmek istiyorum</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>2019-05-16 06:35:01.370</td>\n",
              "      <td>eesmagulbas@gmail.com</td>\n",
              "      <td>Esma Gulbas</td>\n",
              "      <td>1. Seçenek</td>\n",
              "      <td>Orta Seviye</td>\n",
              "      <td>Başlangıç Seviyesi</td>\n",
              "      <td>Başlangıç Seviyesi</td>\n",
              "      <td>Hiç bilmiyorum</td>\n",
              "      <td>Hayır</td>\n",
              "      <td>NaN</td>\n",
              "      <td>Turkcell TPM</td>\n",
              "      <td>Ogrenmek icin</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>2</th>\n",
              "      <td>2019-05-16 06:35:47.923</td>\n",
              "      <td>oktaysabak@yandex.com</td>\n",
              "      <td>oktay sabak</td>\n",
              "      <td>5458497856</td>\n",
              "      <td>Orta Seviye</td>\n",
              "      <td>Hiç bilmiyorum</td>\n",
              "      <td>Hiç bilmiyorum</td>\n",
              "      <td>Başlangıç Seviyesi</td>\n",
              "      <td>Hayır</td>\n",
              "      <td>NaN</td>\n",
              "      <td>startech elektronik / yazılım geliştirici</td>\n",
              "      <td>python becerilerimi arttırmak ve yeni şeyler ö...</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>3</th>\n",
              "      <td>2019-05-16 06:47:47.178</td>\n",
              "      <td>unalzafer061@gmail.com</td>\n",
              "      <td>Ünal Zafer</td>\n",
              "      <td>5535417267</td>\n",
              "      <td>Orta Seviye</td>\n",
              "      <td>Orta Seviye</td>\n",
              "      <td>Başlangıç Seviyesi</td>\n",
              "      <td>Başlangıç Seviyesi</td>\n",
              "      <td>Hayır</td>\n",
              "      <td>NaN</td>\n",
              "      <td>-</td>\n",
              "      <td>-</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>4</th>\n",
              "      <td>2019-05-16 10:08:29.045</td>\n",
              "      <td>batuhatipoglu1@gmail.com</td>\n",
              "      <td>Batu Hatipoğlu</td>\n",
              "      <td>0538 033 90 90</td>\n",
              "      <td>Başlangıç Seviyesi</td>\n",
              "      <td>Hiç bilmiyorum</td>\n",
              "      <td>Hiç bilmiyorum</td>\n",
              "      <td>Hiç bilmiyorum</td>\n",
              "      <td>Evet</td>\n",
              "      <td>2.0</td>\n",
              "      <td>Doğuş Üniversitesi/Elektronik ve Haberleşme Mü...</td>\n",
              "      <td>Birinci eğitimi almıştım ve ikinci eğitimide a...</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div>"
            ],
            "text/plain": [
              "            Zaman damgası  ...           Bu eğitime neden katılmak istiyorsunuz ?\n",
              "0 2019-05-16 05:35:22.919  ...                          Python öğrenmek istiyorum\n",
              "1 2019-05-16 06:35:01.370  ...                                      Ogrenmek icin\n",
              "2 2019-05-16 06:35:47.923  ...  python becerilerimi arttırmak ve yeni şeyler ö...\n",
              "3 2019-05-16 06:47:47.178  ...                                                  -\n",
              "4 2019-05-16 10:08:29.045  ...  Birinci eğitimi almıştım ve ikinci eğitimide a...\n",
              "\n",
              "[5 rows x 12 columns]"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 121
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "vr4pUTX8JQPK",
        "colab_type": "text"
      },
      "source": [
        "### Dictionary'i DataFrame'e Dönüştürme"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "zNbYl5njJYDp",
        "colab_type": "text"
      },
      "source": [
        "pd.DataFrame(dictionary_degiskeni)"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "bXTSVXOaJV00",
        "colab_type": "code",
        "outputId": "e49dd1f8-1100-4b92-9c78-bc6130cd8ca3",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 86
        }
      },
      "source": [
        "ogrenciler ={\"isim\" :[\"Mehmet\",\"Hasibe\",\"Ufuk\"],\n",
        "             \"bolum\" :[\"Akademi\",\"TTECH\",\"DSS\"],\n",
        "             \"yas\":[36,26,35]}\n",
        "\n",
        "\n",
        "ogrenciler_df = pd.DataFrame(ogrenciler)\n",
        "\n",
        "print(ogrenciler_df)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "     isim    bolum  yas\n",
            "0  Mehmet  Akademi   36\n",
            "1  Hasibe    TTECH   26\n",
            "2    Ufuk      DSS   35\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "zkOnaGPKKh8a",
        "colab_type": "text"
      },
      "source": [
        "DataFrame'de istediğimiz sütunu alabiliriz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "8nd0VsCQKmuP",
        "colab_type": "code",
        "outputId": "aa1a9a66-607d-4e83-c1d5-8994e1ece942",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 240
        }
      },
      "source": [
        "ogrenciler ={\"isim\" :[\"Mehmet\",\"Hasibe\",\"Ufuk\"],\n",
        "             \"bolum\" :[\"Akademi\",\"TTECH\",\"DSS\"],\n",
        "             \"yas\":[36,26,35]}\n",
        "\n",
        "\n",
        "ogrenciler_df = pd.DataFrame(ogrenciler)\n",
        "\n",
        "print(ogrenciler_df)\n",
        "print(\"\\n\\n------\\n\\n\")\n",
        "\n",
        "isimler = ogrenciler_df[[\"isim\"]]\n",
        "\n",
        "print(isimler)\n"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "     isim    bolum  yas\n",
            "0  Mehmet  Akademi   36\n",
            "1  Hasibe    TTECH   26\n",
            "2    Ufuk      DSS   35\n",
            "\n",
            "\n",
            "------\n",
            "\n",
            "\n",
            "     isim\n",
            "0  Mehmet\n",
            "1  Hasibe\n",
            "2    Ufuk\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "PUoXouhYLoUr",
        "colab_type": "text"
      },
      "source": [
        "isim ve yaş alalım"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "eK-sxk2TLqQk",
        "colab_type": "code",
        "outputId": "a03a6c6c-0459-40f3-a701-e1019354eb89",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 240
        }
      },
      "source": [
        "ogrenciler ={\"isim\" :[\"Mehmet\",\"Hasibe\",\"Ufuk\"],\n",
        "             \"bolum\" :[\"Akademi\",\"TTECH\",\"DSS\"],\n",
        "             \"yas\":[36,26,35]}\n",
        "\n",
        "\n",
        "ogrenciler_df = pd.DataFrame(ogrenciler)\n",
        "\n",
        "print(ogrenciler_df)\n",
        "print(\"\\n\\n------\\n\\n\")\n",
        "\n",
        "isimler = ogrenciler_df[[\"isim\",\"yas\"]]\n",
        "\n",
        "print(isimler)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "     isim    bolum  yas\n",
            "0  Mehmet  Akademi   36\n",
            "1  Hasibe    TTECH   26\n",
            "2    Ufuk      DSS   35\n",
            "\n",
            "\n",
            "------\n",
            "\n",
            "\n",
            "     isim  yas\n",
            "0  Mehmet   36\n",
            "1  Hasibe   26\n",
            "2    Ufuk   35\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "CHcH74jqh5sf",
        "colab_type": "text"
      },
      "source": [
        "### DataFrame'deki Verilere Ulaşım Yöntemleri"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "0XVTqPwIh9z9",
        "colab_type": "text"
      },
      "source": [
        "loc() metodu ve iloc() metodu kullanılır.\n",
        "\n",
        "> **loc() :** Sütun isimlerini kullanarak verilere erişmenin mümkün olduğu yöntemdir.\n",
        "\n",
        "> **iloc() :** Sütun index veya index aralıklarını kullanarak verilere erişmenin mümkün olduğu yöntemdir.\n",
        "\n",
        "\n",
        "\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "LDjfjuk_L8mS",
        "colab_type": "text"
      },
      "source": [
        "#### iloc() metodu"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "6uSUzqEBMFts",
        "colab_type": "code",
        "outputId": "447b0946-2fef-48f0-8dae-03c07176b128",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 188
        }
      },
      "source": [
        "ogrenciler ={\"isim\" :[\"Mehmet\",\"Hasibe\",\"Ufuk\"],\n",
        "             \"bolum\" :[\"Akademi\",\"TTECH\",\"DSS\"],\n",
        "             \"yas\":[36,26,35]}\n",
        "\n",
        "\n",
        "ogrenciler_df = pd.DataFrame(ogrenciler)\n",
        "\n",
        "print(ogrenciler_df)\n",
        "print(\"\\n\\n------\\n\\n\")\n",
        "\n",
        "isimler = ogrenciler_df.iloc[0,0]\n",
        "\n",
        "print(isimler)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "     isim    bolum  yas\n",
            "0  Mehmet  Akademi   36\n",
            "1  Hasibe    TTECH   26\n",
            "2    Ufuk      DSS   35\n",
            "\n",
            "\n",
            "------\n",
            "\n",
            "\n",
            "Mehmet\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Z0kyH5NqMATF",
        "colab_type": "text"
      },
      "source": [
        "index vererek istediğimiz veriyi çekebliriz."
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "QpFsqM3bgMEz",
        "colab_type": "text"
      },
      "source": [
        "#### loc() metodu"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "11wtQ4-7gN2_",
        "colab_type": "text"
      },
      "source": [
        "Verilen satır numarası ve sütun adı ile erişim sağlanabilir."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "KbSzQhRygYiJ",
        "colab_type": "code",
        "outputId": "228f1d9e-d3d5-4a4b-a0e2-7a4f18a2b440",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 187
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "ogrenciler ={\"isim\" :[\"Mehmet\",\"Hasibe\",\"Ufuk\"],\n",
        "             \"bolum\" :[\"Akademi\",\"TTECH\",\"DSS\"],\n",
        "             \"yas\":[36,26,35]}\n",
        "\n",
        "\n",
        "ogrenciler_df = pd.DataFrame(ogrenciler)\n",
        "\n",
        "print(ogrenciler_df)\n",
        "print(\"\\n\\n------\\n\\n\")\n",
        "\n",
        "isimler = ogrenciler_df.loc[0,\"isim\"]\n",
        "\n",
        "print(isimler)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "     isim    bolum  yas\n",
            "0  Mehmet  Akademi   36\n",
            "1  Hasibe    TTECH   26\n",
            "2    Ufuk      DSS   35\n",
            "\n",
            "\n",
            "------\n",
            "\n",
            "\n",
            "Mehmet\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "tytMF85wgn7r",
        "colab_type": "text"
      },
      "source": [
        "## Slicing işlemi"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "36QTQcIxhVYU",
        "colab_type": "text"
      },
      "source": [
        "iloc metodu ile index aralıkları belirterek istediğimiz satır ve sütunları alabiliriz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "mD-BZQTHgrZk",
        "colab_type": "code",
        "outputId": "a624699b-a19b-4e7d-cf4d-c586716c1cfa",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 255
        }
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "ogrenciler ={\"isim\" :[\"Mehmet\",\"Hasibe\",\"Ufuk\",\"Erdem\",\"Gökhan\"],\n",
        "             \"bolum\" :[\"Akademi\",\"TTECH\",\"DSS\",\"DSS\",\"Toyota\"],\n",
        "             \"yas\":[36,26,35,40,32]}\n",
        "\n",
        "\n",
        "ogrenciler_df = pd.DataFrame(ogrenciler)\n",
        "\n",
        "print(ogrenciler_df)\n",
        "print(\"\\n\\n------\\n\\n\")\n",
        "\n",
        "isimler = ogrenciler_df.iloc[0:2,0:2]\n",
        "\n",
        "print(isimler)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "     isim    bolum  yas\n",
            "0  Mehmet  Akademi   36\n",
            "1  Hasibe    TTECH   26\n",
            "2    Ufuk      DSS   35\n",
            "3   Erdem      DSS   40\n",
            "4  Gökhan   Toyota   32\n",
            "\n",
            "\n",
            "------\n",
            "\n",
            "\n",
            "     isim    bolum\n",
            "0  Mehmet  Akademi\n",
            "1  Hasibe    TTECH\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "9FU-iB7hixUm",
        "colab_type": "text"
      },
      "source": [
        "loc() metodu ile sütun isimleri ile aralıkları belirterek istediğimiz satır ve sütunları alabiliriz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "SIdAC02bitB5",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "import pandas as pd\n",
        "\n",
        "ogrenciler ={\"isim\" :[\"Mehmet\",\"Hasibe\",\"Ufuk\",\"Erdem\",\"Gökhan\"],\n",
        "             \"bolum\" :[\"Akademi\",\"TTECH\",\"DSS\",\"DSS\",\"Toyota\"],\n",
        "             \"yas\":[36,26,35,40,32]}\n",
        "\n",
        "\n",
        "ogrenciler_df = pd.DataFrame(ogrenciler)\n",
        "\n",
        "print(ogrenciler_df)\n",
        "print(\"\\n\\n------\\n\\n\")\n",
        "\n",
        "isimler = ogrenciler_df.loc[0:2,\"bolum\":\"yas\"]\n",
        "\n",
        "print(isimler)"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "53xIbvack4wp",
        "colab_type": "text"
      },
      "source": [
        "## Aşağıdaki url'de bulunan dosyayı indirerek colab'a yüklüyoruz.\n",
        "\n",
        "https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%204/Datasets/TopSellingAlbums.csv\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "QyasZ-XynQ24",
        "colab_type": "text"
      },
      "source": [
        "Dosyamızı yükledikten sonra head metodu ile genel yapısını inceleyelim."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "mS-qgnfPnxoY",
        "colab_type": "code",
        "outputId": "b346ec21-a636-4b3e-c9c4-ef6130d092a3",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 323
        }
      },
      "source": [
        "import pandas as pd\n",
        "# csv_path = \"https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/PY0101EN/Chapter%204/Datasets/TopSellingAlbums.csv\"\n",
        "csv_path = \"TopSellingAlbums.csv\"\n",
        "df = pd.read_csv(csv_path)\n",
        "\n",
        "df.head()"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/html": [
              "<div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>Artist</th>\n",
              "      <th>Album</th>\n",
              "      <th>Released</th>\n",
              "      <th>Length</th>\n",
              "      <th>Genre</th>\n",
              "      <th>Music Recording Sales (millions)</th>\n",
              "      <th>Claimed Sales (millions)</th>\n",
              "      <th>Released.1</th>\n",
              "      <th>Soundtrack</th>\n",
              "      <th>Rating</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>0</th>\n",
              "      <td>Michael Jackson</td>\n",
              "      <td>Thriller</td>\n",
              "      <td>1982</td>\n",
              "      <td>0:42:19</td>\n",
              "      <td>pop, rock, R&amp;B</td>\n",
              "      <td>46.0</td>\n",
              "      <td>65</td>\n",
              "      <td>30-Nov-82</td>\n",
              "      <td>NaN</td>\n",
              "      <td>10.0</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>AC/DC</td>\n",
              "      <td>Back in Black</td>\n",
              "      <td>1980</td>\n",
              "      <td>0:42:11</td>\n",
              "      <td>hard rock</td>\n",
              "      <td>26.1</td>\n",
              "      <td>50</td>\n",
              "      <td>25-Jul-80</td>\n",
              "      <td>NaN</td>\n",
              "      <td>9.5</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>2</th>\n",
              "      <td>Pink Floyd</td>\n",
              "      <td>The Dark Side of the Moon</td>\n",
              "      <td>1973</td>\n",
              "      <td>0:42:49</td>\n",
              "      <td>progressive rock</td>\n",
              "      <td>24.2</td>\n",
              "      <td>45</td>\n",
              "      <td>01-Mar-73</td>\n",
              "      <td>NaN</td>\n",
              "      <td>9.0</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>3</th>\n",
              "      <td>Whitney Houston</td>\n",
              "      <td>The Bodyguard</td>\n",
              "      <td>1992</td>\n",
              "      <td>0:57:44</td>\n",
              "      <td>R&amp;B, soul, pop</td>\n",
              "      <td>27.4</td>\n",
              "      <td>44</td>\n",
              "      <td>17-Nov-92</td>\n",
              "      <td>Y</td>\n",
              "      <td>8.5</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>4</th>\n",
              "      <td>Meat Loaf</td>\n",
              "      <td>Bat Out of Hell</td>\n",
              "      <td>1977</td>\n",
              "      <td>0:46:33</td>\n",
              "      <td>hard rock, progressive rock</td>\n",
              "      <td>20.6</td>\n",
              "      <td>43</td>\n",
              "      <td>21-Oct-77</td>\n",
              "      <td>NaN</td>\n",
              "      <td>8.0</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div>"
            ],
            "text/plain": [
              "            Artist                      Album  ...  Soundtrack Rating\n",
              "0  Michael Jackson                   Thriller  ...         NaN   10.0\n",
              "1            AC/DC              Back in Black  ...         NaN    9.5\n",
              "2       Pink Floyd  The Dark Side of the Moon  ...         NaN    9.0\n",
              "3  Whitney Houston              The Bodyguard  ...           Y    8.5\n",
              "4        Meat Loaf            Bat Out of Hell  ...         NaN    8.0\n",
              "\n",
              "[5 rows x 10 columns]"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 4
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "ONOLFamzoURo",
        "colab_type": "text"
      },
      "source": [
        "Datasetimizde belirlediğimiz sütunu unique olarak yazdıralım."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "ABrZhC1Eo8GH",
        "colab_type": "code",
        "outputId": "7b035aae-27a0-430c-aa7c-299593afcb14",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "import pandas as pd\n",
        "#csv_path =\"dsdasds\"\n",
        "csv_path = \"TopSellingAlbums.csv\"\n",
        "df = pd.read_csv(csv_path)\n",
        "\n",
        "#df[\"Released\"]\n",
        "\n",
        "df[\"Released\"].unique()"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "array([1982, 1980, 1973, 1992, 1977, 1976])"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 5
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Tvwh7z5bpghp",
        "colab_type": "text"
      },
      "source": [
        "### Bir sütundaki belli değerleri almak"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "ssYfHic3py1k",
        "colab_type": "text"
      },
      "source": [
        "Aşağıdaki\n",
        "\n",
        "> df[\"Released\"]>0\n",
        "\n",
        "Her bir satır için True ya da False dönecektir.\n",
        "\n"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "lmdWYWaYpu0e",
        "colab_type": "code",
        "outputId": "a462410a-9641-4e18-bcd9-2c2578de63b3",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 170
        }
      },
      "source": [
        "import pandas as pd\n",
        "#csv_path =\"dsdasds\"\n",
        "csv_path = \"TopSellingAlbums.csv\"\n",
        "df = pd.read_csv(csv_path)\n",
        "\n",
        "#df[\"Released\"]\n",
        "\n",
        "df[\"Released\"]>0"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "0    True\n",
              "1    True\n",
              "2    True\n",
              "3    True\n",
              "4    True\n",
              "5    True\n",
              "6    True\n",
              "7    True\n",
              "Name: Released, dtype: bool"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 7
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "YsTNCrUorA3X",
        "colab_type": "text"
      },
      "source": [
        "### Yukarıda bulduğumuz her satır için True False değerlerini DataFrame'de koşul olarak kullanalım ve uygun verileri yazdıralım."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "p-P-IgWUrTUd",
        "colab_type": "code",
        "outputId": "deb9ffd5-9af9-4a52-c2b8-a395ce07b172",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 227
        }
      },
      "source": [
        "import pandas as pd\n",
        "#csv_path =\"dsdasds\"\n",
        "csv_path = \"TopSellingAlbums.csv\"\n",
        "df = pd.read_csv(csv_path)\n",
        "\n",
        "\n",
        "df[df[\"Released\"]>=1980]"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/html": [
              "<div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>Artist</th>\n",
              "      <th>Album</th>\n",
              "      <th>Released</th>\n",
              "      <th>Length</th>\n",
              "      <th>Genre</th>\n",
              "      <th>Music Recording Sales (millions)</th>\n",
              "      <th>Claimed Sales (millions)</th>\n",
              "      <th>Released.1</th>\n",
              "      <th>Soundtrack</th>\n",
              "      <th>Rating</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>0</th>\n",
              "      <td>Michael Jackson</td>\n",
              "      <td>Thriller</td>\n",
              "      <td>1982</td>\n",
              "      <td>0:42:19</td>\n",
              "      <td>pop, rock, R&amp;B</td>\n",
              "      <td>46.0</td>\n",
              "      <td>65</td>\n",
              "      <td>30-Nov-82</td>\n",
              "      <td>NaN</td>\n",
              "      <td>10.0</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>AC/DC</td>\n",
              "      <td>Back in Black</td>\n",
              "      <td>1980</td>\n",
              "      <td>0:42:11</td>\n",
              "      <td>hard rock</td>\n",
              "      <td>26.1</td>\n",
              "      <td>50</td>\n",
              "      <td>25-Jul-80</td>\n",
              "      <td>NaN</td>\n",
              "      <td>9.5</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>3</th>\n",
              "      <td>Whitney Houston</td>\n",
              "      <td>The Bodyguard</td>\n",
              "      <td>1992</td>\n",
              "      <td>0:57:44</td>\n",
              "      <td>R&amp;B, soul, pop</td>\n",
              "      <td>27.4</td>\n",
              "      <td>44</td>\n",
              "      <td>17-Nov-92</td>\n",
              "      <td>Y</td>\n",
              "      <td>8.5</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div>"
            ],
            "text/plain": [
              "            Artist          Album  Released  ... Released.1 Soundtrack  Rating\n",
              "0  Michael Jackson       Thriller      1982  ...  30-Nov-82        NaN    10.0\n",
              "1            AC/DC  Back in Black      1980  ...  25-Jul-80        NaN     9.5\n",
              "3  Whitney Houston  The Bodyguard      1992  ...  17-Nov-92          Y     8.5\n",
              "\n",
              "[3 rows x 10 columns]"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 8
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "ez7fv_O4rfzD",
        "colab_type": "text"
      },
      "source": [
        "### Yukarıda 1980 ve sonrasında çıkan albümleri listelediğimiz verimizi yeni bir csv dosyasına yazalım."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "YtZEte9arqG3",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "import pandas as pd\n",
        "#csv_path =\"dsdasds\"\n",
        "csv_path = \"TopSellingAlbums.csv\"\n",
        "df = pd.read_csv(csv_path)\n",
        "\n",
        "\n",
        "df_new = df[df[\"Released\"]>=1980]\n",
        "\n",
        "df_new.to_csv(\"NewAlbums.csv\")"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "lCZ4hS_-twMP",
        "colab_type": "text"
      },
      "source": [
        "Aşağıdaki görüldüğü gibi yukarıdaki kodu çalıştırdığımızda File kısmında NewAlbums.csv dosyamız oluştu."
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "yehYhVmGsf4d",
        "colab_type": "text"
      },
      "source": [
        "![alt text](https://firebasestorage.googleapis.com/v0/b/python-dec9c.appspot.com/o/ss_newalbums.png?alt=media&token=283acb97-f4cf-4626-876a-42ed36724c65)"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "10INzKK1KkPa",
        "colab_type": "text"
      },
      "source": [
        "## Numpy"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "pu2OHsW_KoCO",
        "colab_type": "text"
      },
      "source": [
        "Matematiksel hesaplamalar için kullanılan en yaygın kütüphanedir.\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "ION4sH6YMw9e",
        "colab_type": "text"
      },
      "source": [
        "### import"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "YvLydvqVIy8u",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "import numpy as np\n",
        "import time"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "wmjh69_ONA6X",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "x = np.random.random(100000000)\n",
        "#print(x)"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "DNhgV3OVNj0R",
        "colab_type": "text"
      },
      "source": [
        "### İşlemin süresini python ile hesaplayalım\n"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "Uxs7xOZmNn1t",
        "colab_type": "code",
        "outputId": "36cc90bb-70f6-4102-dd3a-646dc512aed1",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "start = time.time()\n",
        "sum(x) / len(x)\n",
        "print(time.time() - start)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "9.28833532333374\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "yIf8u-91QqLh",
        "colab_type": "text"
      },
      "source": [
        "### İşlem süresini numpy ile hesaplayalım"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "kC59MVfSRDu6",
        "colab_type": "code",
        "outputId": "87f7131d-65b2-44c3-995b-afdb97f0e68b",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "start = time.time()\n",
        "np.mean(x)\n",
        "print(time.time() - start)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "0.1302661895751953\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "_eji27_cRfZk",
        "colab_type": "text"
      },
      "source": [
        "## Numpy ile temel liste işlemleri\n",
        "\n"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "FJo_0bDtX8Xk",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "import numpy as np\n",
        "x = np.array([1,2,3,4,5])\n"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "9c2AjeX8aOLW",
        "colab_type": "text"
      },
      "source": [
        "### Dizinin tipini yazdırmak için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "GCA-90a-ZFNU",
        "colab_type": "code",
        "outputId": "85baaf65-82b7-451d-d188-09e7d1e0d7f1",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "print(x)\n",
        "print(type(x))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 2 3 4 5]\n",
            "<class 'numpy.ndarray'>\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "DLQSEEzxahKi",
        "colab_type": "text"
      },
      "source": [
        "### Dizinin içindeki verilerin tipini yazdırmak için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "OxtUVp1aZ96d",
        "colab_type": "code",
        "outputId": "3df157b6-5f33-46bb-d57b-fd0115ae7407",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "print(x.dtype)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "int64\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "3fQV-HgWamb_",
        "colab_type": "text"
      },
      "source": [
        "### Dizinin boyutunu yazdırmak için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "UI9j-illbd6n",
        "colab_type": "code",
        "outputId": "2f92c84b-c578-410d-a28a-bb67d0db5a7f",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x.shape"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "(5,)"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 17
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "E3OsyN9xb4kG",
        "colab_type": "text"
      },
      "source": [
        "### İki boyutlu dizi oluşturmak için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "AIHus0Pvb8Im",
        "colab_type": "code",
        "outputId": "81f6b3c9-0e92-458a-eec3-6fa701e719ff",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 85
        }
      },
      "source": [
        "y= np.array([[1,2,3],[4,5,6],[7,8,9],[10,11,12]])\n",
        "print(y)\n",
        "\n"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[ 1  2  3]\n",
            " [ 4  5  6]\n",
            " [ 7  8  9]\n",
            " [10 11 12]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "mmmgclhgeYCX",
        "colab_type": "text"
      },
      "source": [
        "### Dizinin boyutunu yazdırmak için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "hg4BxjHheYZ9",
        "colab_type": "code",
        "outputId": "c0386b7d-03c3-43d2-a471-5745118bc2c1",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "print(y.shape)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "(4, 3)\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "nppevG7AfxIk",
        "colab_type": "text"
      },
      "source": [
        "### Dizideki eleman sayını yazdırmak için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "k12rn7oujy_c",
        "colab_type": "code",
        "outputId": "7c10ea4c-34a2-4787-b031-c5e925c8c7b9",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "y.size"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "12"
            ]
          },
          "metadata": {
            "tags": []
          },
          "execution_count": 31
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "V6Wx2XQWkXoK",
        "colab_type": "text"
      },
      "source": [
        "## String dizisi:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "r3ZvF4lMkZ3h",
        "colab_type": "code",
        "outputId": "5e199ed2-2748-48f8-d79e-47b2f11c928f",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.array(['Hi','Guys'])\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "['Hi' 'Guys']\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "qRzr7SEDlBFE",
        "colab_type": "text"
      },
      "source": [
        "### Shape,type,dtype"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "1PzlasFelH__",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "print('shape',x.shape)\n",
        "print('type',type(x))\n",
        "print('dtype',x.dtype)"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "D795tSsAGJMp",
        "colab_type": "text"
      },
      "source": [
        "Farklı tipler olan dizilerde örneğin int ve string gibi ortak upcast olamayacak tiplerde (Uxx) tipine cast edilir."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "M_gRFPxxDpcP",
        "colab_type": "code",
        "outputId": "e92d44e0-0169-4fe7-ce0c-d912602e3f84",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 85
        }
      },
      "source": [
        "x = np.array([1,2,3,4.1,'World'])\n",
        "print(x)\n",
        "print('shape',x.shape)\n",
        "print('type',type(x))\n",
        "print('dtype',x.dtype)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "['1' '2' '3' '4.1' 'World']\n",
            "shape (5,)\n",
            "type <class 'numpy.ndarray'>\n",
            "dtype <U32\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "s48OBQ_O_D1X",
        "colab_type": "text"
      },
      "source": [
        "**nparray'de tüm veri tipleri aynı olmak zorundadır.** Farklı tipler bulunduran dizide veri tipi  veri kaybı yaşanmaması için içerdeki en büyük veri tipine çevrilir. Buna **upcasting** denir. Örneğin int ve float olan bir dizide tipler float olarak tutulur."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "gdC2d7tnGa16",
        "colab_type": "code",
        "outputId": "2ef385ab-f7ac-4936-c3d8-5610ec6bbec7",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.array([1,3.5,5])\n",
        "print(x,x.dtype)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1.  3.5 5. ] float64\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "qwWbFsLTGw-E",
        "colab_type": "text"
      },
      "source": [
        "np array'de tutulan veriler farklı tipte iken tutmasını istediğimiz veri tipini kendimiz belirtebiliriz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "zlnvsNYvG5_b",
        "colab_type": "code",
        "outputId": "0c4ef905-c594-42e5-ff60-2c48aa278e57",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "x = np.array([1.5,2.2,3.7,9,10], dtype = np.int64)\n",
        "print(x)\n",
        "print('dtype',x.dtype)\n"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[ 1  2  3  9 10]\n",
            "dtype int64\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "6VnUzLG-Hj_U",
        "colab_type": "text"
      },
      "source": [
        "## nparray'i Dosyaya Kaydetme"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "GZGc3nr0I8Uz",
        "colab_type": "text"
      },
      "source": [
        "numpy kütüphanesinin okuyabileceği formatta dosyaya yazılır. Bu dosyanın uzantısı **.npy** olarak kaydedilir.\n",
        "Not defteri vs açtığınızda veriyi direkt görüntüleyemezsiniz. numpy kütüphanesi kullanarak programatik olarak erişebiliriz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "SiQE2rBuIND6",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "x = np.array([1,3.5,5])\n",
        "np.save('dizi_dosyasi',x)"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "KpIwyrRfJV_r",
        "colab_type": "text"
      },
      "source": [
        "## nparray'i Dosyadan Okuma"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "FeeIeVl0Jan3",
        "colab_type": "code",
        "outputId": "4769f31d-9c96-4db9-df98-4532acf719bd",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "y = np.load('dizi_dosyasi.npy')\n",
        "print(y)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1.  3.5 5. ]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "c6VCfLIgIUB1",
        "colab_type": "text"
      },
      "source": [
        "## Dizinin elemanın erişme, silme, eleman ekleme"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "KNWW1XLaIcpK",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "import numpy as np"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "l2tMLygrIoja",
        "colab_type": "code",
        "outputId": "1e0fac09-3772-4c02-8aaa-b718634f3da8",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.array([1,2,3,4,5])\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 2 3 4 5]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "RpIHfnK1I-lB",
        "colab_type": "code",
        "outputId": "6782c0f0-4c8b-4147-a3e2-65f867473753",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "print('1nd element:',x[0])\n",
        "print('2nd element:',x[1])\n",
        "print('5 element:',x[4])\n"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "1nd element: 1\n",
            "2nd element: 2\n",
            "5 element: 5\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Wm01mOyxJbMk",
        "colab_type": "text"
      },
      "source": [
        "index (-) verdiğimizde son elemandan -1 diymeye saymaya başlarız. Örneğin:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "jUypS-XfJkcs",
        "colab_type": "code",
        "outputId": "4f465e75-34fe-41e5-be3b-2481ad9c7218",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "print('1nd element:',x[-5])\n",
        "print('2nd element:',x[-4])\n",
        "print('5 element:',x[-1])"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "1nd element: 1\n",
            "2nd element: 2\n",
            "5 element: 5\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "dM0F6NglJ9eS",
        "colab_type": "text"
      },
      "source": [
        "**Dizideki elemanı değiştirmek için :**"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "VBWtyysxKJBu",
        "colab_type": "code",
        "outputId": "86f9ca89-0aaf-4923-8c8b-3b716441fcf0",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x[3] = 20\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[ 1  2  3 20  5]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "d227KHn9hmJM",
        "colab_type": "text"
      },
      "source": [
        "## arange() ve reshape()"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "6b6e8Mqkhrca",
        "colab_type": "text"
      },
      "source": [
        "**arange()** metodu içerisine iki int parametre alır ve o aralıktaki sayıları dizimiz için üretir.\n",
        "\n",
        "**reshape() ** metodu dizimizin satır ve sütun boyutlarını değiştirebilmemizi sağlar.\n",
        "\n",
        "Not: arrange ve reshape kullanırken reshape ettiğiniz boyutta verinizin olması gerekir. Fazla ya da eksik olduğunda reshape edemediği için hata verir."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "__hMlEa7h9dm",
        "colab_type": "code",
        "outputId": "8333c517-f7cd-4236-9e57-07c251c1b607",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "x = np.arange(1,13).reshape(3,4)\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[ 1  2  3  4]\n",
            " [ 5  6  7  8]\n",
            " [ 9 10 11 12]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "LqrQSxhTjkJy",
        "colab_type": "text"
      },
      "source": [
        "0. satırın 0. elemanı şeklinde print edebiliriz."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "XK6AiPGFjpS8",
        "colab_type": "code",
        "outputId": "900fe94a-081d-4a28-829e-3983e016b43f",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "print('Element at (0,0):', x[0,0])\n",
        "print('Element at (0,1):', x[0,1])\n",
        "print('Element at (2,3):', x[2,3])"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Element at (0,0): 1\n",
            "Element at (0,1): 2\n",
            "Element at (2,3): 12\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "ekKUeiExkCLi",
        "colab_type": "text"
      },
      "source": [
        "Dizideki istediğimiz satır ve sütundaki elemanı değiştirmek için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "4kH0Z2pCkIdg",
        "colab_type": "code",
        "outputId": "47476e50-4447-4037-f2da-b4774a20e134",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "x[0,0] = 15\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[15  2  3  4]\n",
            " [ 5  6  7  8]\n",
            " [ 9 10 11 12]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "TSl8Cg8Wl7I9",
        "colab_type": "text"
      },
      "source": [
        "## delete() metodu"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "QGx1pIX_l_JV",
        "colab_type": "code",
        "outputId": "08b83ecc-2cde-47a9-a847-0994aa5701ee",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.array([0,1,2,3,4,5])\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[0 1 2 3 4 5]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "hGojYTvUmHX9",
        "colab_type": "code",
        "outputId": "ac7985b6-9ecf-4ed9-ef85-83968807f676",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.delete(x,[0,4])\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 2 3 5]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "6e4bBFhlmjXy",
        "colab_type": "text"
      },
      "source": [
        "Eğer dizimiz 1den fazla satırdan oluşuyorsa dilediğimiz satırı silmek için:\n",
        "\n"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "QfsMHkvumUKb",
        "colab_type": "code",
        "outputId": "477577e9-9b72-49ea-894f-1ab043a8f9dc",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "y = np.arange(1,10).reshape(3,3)\n",
        "print(y)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[1 2 3]\n",
            " [4 5 6]\n",
            " [7 8 9]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "pv2kVIOzqFBO",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "w = np.delete(y,0,axis=0)\n",
        "print(w)"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "89DWR1K0sQbH",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "v = np.delete(y,[0,2],axis=1)\n",
        "print(v)"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "2kahxnY8skcx",
        "colab_type": "text"
      },
      "source": [
        "## append() methodu"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "n_kA4vAYsozK",
        "colab_type": "code",
        "outputId": "d5a0f02e-e6f6-4534-c318-f6a89dd9e6c7",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.array([1,2,3,4,5])\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 2 3 4 5]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "G8deJHCRsv9o",
        "colab_type": "code",
        "outputId": "2dae22d7-c7a8-44ec-9a9d-60a5b22b52da",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.append(x,6)\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 2 3 4 5 6]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "6sOvUS_ms5my",
        "colab_type": "code",
        "outputId": "d3c41588-61c9-47f6-adce-3861b6d728d0",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.append(x,[7,8])\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 2 3 4 5 6 7 8]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "D5spRwkwte_r",
        "colab_type": "text"
      },
      "source": [
        "Eğer dizimiz 1den fazla satırdan oluşuyorsa yeni satur ya da sütun eklemek için:\n",
        "\n"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "8-y00ZbitjJw",
        "colab_type": "code",
        "outputId": "4f049435-8338-44e3-b540-1d0249b4069e",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "y = np.arange(1,10).reshape(3,3)\n",
        "print(y)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[1 2 3]\n",
            " [4 5 6]\n",
            " [7 8 9]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "ZYbsTMfxtsYy",
        "colab_type": "code",
        "outputId": "12375066-6d8b-4d7e-e55f-ca40cfc3a854",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 85
        }
      },
      "source": [
        "w = np.append(y,[[10,11,12]],axis=0)\n",
        "print(w)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[ 1  2  3]\n",
            " [ 4  5  6]\n",
            " [ 7  8  9]\n",
            " [10 11 12]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "Y10VYrHzt8Pa",
        "colab_type": "code",
        "outputId": "569da458-6236-4d8c-8783-2c7f33156a5e",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "v = np.append(y,[[10],[11],[12]],axis=1)\n",
        "print(v)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[ 1  2  3 10]\n",
            " [ 4  5  6 11]\n",
            " [ 7  8  9 12]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "vsxdVmuduIxq",
        "colab_type": "text"
      },
      "source": [
        "## insert() metodu"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "5WDpEYNTuhlU",
        "colab_type": "text"
      },
      "source": [
        "Eğer dizide istediğimiz bir index'e eleman eklemek istiyorsak insert() metodunu kullanırız."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "mk9Tit_TuqAc",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "x = np.array([1,2,5,6,7])\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "tm4_eKtcuzyt",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "x = np.insert(x,2,[3,4])\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "nHuWqsvNu-xy",
        "colab_type": "text"
      },
      "source": [
        "Eğer dizimiz birden fazla satırdan oluşuyorsa:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "8XEnr7siu-dF",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "y = np.array([[1,2,3],[7,8,9]])\n",
        "print(y)"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "uwPWVcSmvNyF",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "w = np.insert(y,1,[4,5,6],axis=0)\n",
        "print(w)"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "6CWPE90C1Zum",
        "colab_type": "text"
      },
      "source": [
        "## İki diziyi birleştirmek için: vstack() ve hstack() metodları\n",
        "\n"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "5shvivTk2BM3",
        "colab_type": "text"
      },
      "source": [
        "Burada x ve y adında iki ayrı dizi oluşturacağız. \n",
        "vstack() metodu ile iki diziyi birleştirip z dizisine atayacağız. \n",
        "\n",
        "**vstack()** metodu dizileri alt alta satır olarak (vertical) birleştirir. "
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "zKt4PoLj1fY7",
        "colab_type": "code",
        "outputId": "34d2c3b1-2a32-4df1-9e05-420b5238b4b2",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.array([1,2])\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 2]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "NAAJewtz1pdr",
        "colab_type": "code",
        "outputId": "76f894b6-4890-415b-bc57-5cf6568439c6",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "y = np.array([[3,4],[5,6]])\n",
        "print(y)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[3 4]\n",
            " [5 6]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "RMVhiOat1zv3",
        "colab_type": "code",
        "outputId": "b534b0ef-acb9-4219-f334-9efcd80d9827",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "z = np.vstack((x,y))\n",
        "print(z)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[1 2]\n",
            " [3 4]\n",
            " [5 6]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "geZR4toN2oiF",
        "colab_type": "text"
      },
      "source": [
        "## hstack() metodu"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "qr8rhPFs2yJT",
        "colab_type": "text"
      },
      "source": [
        "hstack() metodu ise dizileri yatayda birleştirir (horizontal)"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "29jCc3mG23tU",
        "colab_type": "code",
        "outputId": "cc176fe6-e26c-4186-92b7-5a14ffd99d68",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "w = np.hstack((y,x.reshape(2,1)))\n",
        "print(w)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[3 4 1]\n",
            " [5 6 2]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Po4RNCik7oPH",
        "colab_type": "text"
      },
      "source": [
        "# Boolean Indexing, Set Operations, and Sorting\n",
        "\n"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "pDic1-cc7u0x",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "import numpy as np"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "VNE-zrTF70jx",
        "colab_type": "code",
        "outputId": "7788591f-ac34-4383-9a98-8bee59194e69",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 102
        }
      },
      "source": [
        "x = np.arange(25).reshape(5,5)\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[ 0  1  2  3  4]\n",
            " [ 5  6  7  8  9]\n",
            " [10 11 12 13 14]\n",
            " [15 16 17 18 19]\n",
            " [20 21 22 23 24]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "aEgeK7-W8eFK",
        "colab_type": "text"
      },
      "source": [
        "Dizimizi yazdırırken 10'dan büyük olan elemanlarını yazdırmak için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "whJLi7808DUg",
        "colab_type": "code",
        "outputId": "5cba8fc7-b96d-44e7-a3ac-d79a94360ba5",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "print(x[x>10])"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[11 12 13 14 15 16 17 18 19 20 21 22 23 24]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Q7Kilg6J8f3M",
        "colab_type": "text"
      },
      "source": [
        "7'den küçük eşit olan elemanları yazdırmak için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "A50bYmKj9MWD",
        "colab_type": "code",
        "outputId": "712931d0-0baf-44f0-ffed-c2201a1b8328",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "print(x[x<=7])"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[0 1 2 3 4 5 6 7]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "aa9png599X5k",
        "colab_type": "text"
      },
      "source": [
        "10'dan büyük, 17'den küçük elemanları yazdırmak için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "mRpB6rBK9fVw",
        "colab_type": "code",
        "outputId": "3b614ad4-f6f5-44b3-f342-1c3acbf553e5",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "print(x[(x>10) & (x<17) ])"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[11 12 13 14 15 16]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "3R2bgZEE-Qwt",
        "colab_type": "text"
      },
      "source": [
        "10'dan büyük ve 17'den küçük olan elemanlara -1 atamak için:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "fuizP1nP-Sj7",
        "colab_type": "code",
        "outputId": "99cb5092-9dc2-4cf3-ff11-07d4e7893509",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 102
        }
      },
      "source": [
        "x[(x>10) & (x<17)] = -1\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[ 0  1  2  3  4]\n",
            " [ 5  6  7  8  9]\n",
            " [10 -1 -1 -1 -1]\n",
            " [-1 -1 17 18 19]\n",
            " [20 21 22 23 24]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "OUgChy77-30Z",
        "colab_type": "text"
      },
      "source": [
        "# intersection, difference, union"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "jJXDOwS4-9qs",
        "colab_type": "text"
      },
      "source": [
        "## intersect1d() metodu :\n",
        "İki dizideki ortak elemanları bulan metoddur."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "NSYQbPmC_1o_",
        "colab_type": "code",
        "outputId": "5b9933fc-b127-4b24-83da-591c99baabce",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.array([1,2,3,4,5])\n",
        "y = np.array([6,7,2,8,4])\n",
        "\n",
        "print(np.intersect1d(x,y))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[2 4]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "ob6r-xIX_zCz",
        "colab_type": "text"
      },
      "source": [
        "## setdiff1d() metodu:"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "V2v9faQXAzyA",
        "colab_type": "text"
      },
      "source": [
        "İki dizideki farklı olan elemanları bulur."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "ViqKJVBRA4CM",
        "colab_type": "code",
        "outputId": "f99e7167-08a8-46e2-dbed-3e99c30ff602",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "print(np.setdiff1d(x,y))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 3 5]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "NxN17BykA8_s",
        "colab_type": "text"
      },
      "source": [
        "## union1d() metodu:"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "sCB179DcBFY6",
        "colab_type": "text"
      },
      "source": [
        "İki dizideki tüm elemanları unique şekilde yazdırır"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "pSD0_HTCBJ5B",
        "colab_type": "code",
        "outputId": "f6bd8d0c-3274-4ebb-96f5-84240e0e4163",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "print(np.union1d(x,y))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 2 3 4 5 6 7 8]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "l2exTXRREknm",
        "colab_type": "text"
      },
      "source": [
        "# np.sort() fonksiyonu ile sort metodunun farkı"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "E2InLVMZEtNl",
        "colab_type": "text"
      },
      "source": [
        "np.sort() = İşlemi bellekte yapar, orjinali değiştirmez.\n",
        ".sort = Orjinal diziyi değiştirir."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "ZjFFGFiwFIxR",
        "colab_type": "code",
        "outputId": "8ee33ded-237b-4b03-85f3-0bd6b6ebf723",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x = np.random.randint(1,11, size = (10,))\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[ 9  6 10  4  9  3  1  3  5  8]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "Em5sKhQLGUT-",
        "colab_type": "text"
      },
      "source": [
        "## np.sort() örneği:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "oIxuOi7xFoy_",
        "colab_type": "code",
        "outputId": "57a7a5cb-4de5-4c61-a2de-a804c1af763f",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "print(np.sort(x))\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[ 1  3  3  4  5  6  8  9  9 10]\n",
            "[ 9  6 10  4  9  3  1  3  5  8]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "9RRODtJrGXjI",
        "colab_type": "text"
      },
      "source": [
        "## x.sort() örneği:"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "YEow0lb2F0ve",
        "colab_type": "code",
        "outputId": "c18885f5-b258-4070-cf69-edb64ac13377",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "x.sort()\n",
        "print(x)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[ 1  3  3  4  5  6  8  9  9 10]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "m_Nf9RxeFlGO",
        "colab_type": "text"
      },
      "source": [
        "## Çok boyutlu dizilerde sort() işlemi"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "MIoiz1giGrbu",
        "colab_type": "text"
      },
      "source": [
        "Birden fazla satırdan oluşan dizilerde x'e göre ya da y'ye göre sıralama yapabiliriz. Bunun için sort metoduna \n",
        "\n",
        "### axis=0 \n",
        "Sütunları kendi içinde sıralar, \n",
        "\n",
        "### axis=1 \n",
        "Satırları kendi içinde sıralar."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "Ov9DSiyqHCPp",
        "colab_type": "code",
        "outputId": "8d9abcdd-f309-4202-fa24-4a910c1a0667",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 102
        }
      },
      "source": [
        "x = np.random.randint(1,11,size=(5,5))\n",
        "print(x)\n"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[7 6 3 7 9]\n",
            " [3 6 5 7 5]\n",
            " [6 1 7 4 5]\n",
            " [5 1 5 2 9]\n",
            " [1 2 6 9 3]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "pBLsM08FHWBQ",
        "colab_type": "code",
        "outputId": "344922ad-eb4d-4dd3-ffb0-c1efa361a806",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 119
        }
      },
      "source": [
        "print('Sütunlar kendi içinde sıralandığında:')\n",
        "print(np.sort(x, axis = 0))\n"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Sütunlar kendi içinde sıralandığında:\n",
            "[[1 1 3 2 3]\n",
            " [3 1 5 4 5]\n",
            " [5 2 5 7 5]\n",
            " [6 6 6 7 9]\n",
            " [7 6 7 9 9]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "_ERZh4fNH2Cp",
        "colab_type": "code",
        "outputId": "8e23466f-6499-4147-dc80-0e6d766050bf",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 119
        }
      },
      "source": [
        "print('Satırları kendi içinde sıralandığında:')\n",
        "print(np.sort(x, axis = 1))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Satırları kendi içinde sıralandığında:\n",
            "[[3 6 7 7 9]\n",
            " [3 5 5 6 7]\n",
            " [1 4 5 6 7]\n",
            " [1 2 5 5 9]\n",
            " [1 2 3 6 9]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "jNLOsowjRMVc",
        "colab_type": "text"
      },
      "source": [
        "# Aritmetik Operatörler"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "yXoo3lgmRPo1",
        "colab_type": "text"
      },
      "source": [
        "## add() \n",
        "Toplama işlemi için kullanılır"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "6CZtfLFqRhD1",
        "colab_type": "code",
        "colab": {}
      },
      "source": [
        "import numpy as np"
      ],
      "execution_count": 0,
      "outputs": []
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "tbVJULlGRlfw",
        "colab_type": "code",
        "outputId": "f16d9c9d-c7bc-4d4e-94d0-98dfec83f494",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "x = np.array([1,2,3,4])\n",
        "y = np.array([5,6,7,8])\n",
        "\n",
        "print(x)\n",
        "print(y)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 2 3 4]\n",
            "[5 6 7 8]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "nY51ercvRxoo",
        "colab_type": "code",
        "outputId": "5294269b-a778-48e9-dc6b-4dac6dd9ae17",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "print(x+y)"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[ 6  8 10 12]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "nZJjlTWtR1kX",
        "colab_type": "code",
        "outputId": "088e024e-1b4a-4d3e-b76f-eed3ea1b7ecc",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 34
        }
      },
      "source": [
        "print(np.add(x,y))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[ 6  8 10 12]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "mHh_0ZqLSEkn",
        "colab_type": "text"
      },
      "source": [
        "## subtract()"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "XdLkrAD8SGsP",
        "colab_type": "text"
      },
      "source": [
        "Çıkarma işlemi"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "YYvbixYHSNO7",
        "colab_type": "code",
        "outputId": "af196843-826b-43b0-be29-71b733ee0f58",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "print(x-y)\n",
        "print(np.subtract(x,y))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[-4 -4 -4 -4]\n",
            "[-4 -4 -4 -4]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "7VZfWHa7SVIl",
        "colab_type": "text"
      },
      "source": [
        "## multiply()"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "vS6y6eaFSXdO",
        "colab_type": "text"
      },
      "source": [
        "Çarpma işlemi"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "N1XZXxyxSY79",
        "colab_type": "code",
        "outputId": "b8426c8c-1c0f-4e18-e982-b2165a8f0809",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "print(x*y)\n",
        "print(np.multiply(x,y))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[ 5 12 21 32]\n",
            "[ 5 12 21 32]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "p5F-qbr5ShMO",
        "colab_type": "text"
      },
      "source": [
        "## divide()"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "vmOYvVteSfub",
        "colab_type": "code",
        "outputId": "3bbe2f2d-879c-4078-b258-f59020a3c4d0",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "print(x/y)\n",
        "print(np.divide(x,y))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[0.2        0.33333333 0.42857143 0.5       ]\n",
            "[0.2        0.33333333 0.42857143 0.5       ]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "1m4b1LQ0Tu7N",
        "colab_type": "text"
      },
      "source": [
        "## exp(), sqrt(), pow()"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "AW6wv3Q0T_AW",
        "colab_type": "code",
        "outputId": "dea5b451-fc8e-408c-b078-b25b0f31022c",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 221
        }
      },
      "source": [
        "x = np.array([1,2,3,4])\n",
        "print(x)\n",
        "\n",
        "print('x dizisinin tüm elemanlarının Exponansiyeli = \\n', np.exp(x),'\\n')\n",
        "print('x dizisinin tüm elemanlarının Karekökü = \\n\\n',np.sqrt(x),'\\n')\n",
        "print('x dizisinin tüm elemanlarının Karesi) = \\n\\n',np.power(x,2),'\\n')\n"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[1 2 3 4]\n",
            "x dizisinin tüm elemanlarının Exponansiyeli = \n",
            " [ 2.71828183  7.3890561  20.08553692 54.59815003] \n",
            "\n",
            "x dizisinin tüm elemanlarının Karekökü = \n",
            "\n",
            " [1.         1.41421356 1.73205081 2.        ] \n",
            "\n",
            "x dizisinin tüm elemanlarının Karesi) = \n",
            "\n",
            " [ 1  4  9 16] \n",
            "\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "9jWq1aQ-VDeo",
        "colab_type": "text"
      },
      "source": [
        "## mean(), sum(), std(), median(), max(), min()"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "bOGogY8MVRl4",
        "colab_type": "code",
        "outputId": "fd43e6cb-d157-4f69-eabc-a5fa3c4f2a5b",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 51
        }
      },
      "source": [
        "x = np.array([[1,2], [3,4]])\n",
        "print(x)\n"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "[[1 2]\n",
            " [3 4]]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "dp5XVF_SXVkP",
        "colab_type": "text"
      },
      "source": [
        "### mean()"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "j_fsTI4CWuCm",
        "colab_type": "code",
        "outputId": "2d2d30ea-5871-4b65-ebd8-5c1e500c4871",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "print('X dizisinin tüm elemanlarının ortalaması:', X.mean())\n",
        "print('X dizisinin sütunlarının ortalaması :', X.mean(axis=0))\n",
        "print('X dizisinin satırlarının ortalaması:', X.mean(axis=1))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "X dizisinin tüm elemanlarının ortalaması: 2.5\n",
            "X dizisinin sütunlarının ortalaması : [2. 3.]\n",
            "X dizisinin satırlarının ortalaması: [1.5 3.5]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "cLRTXheMXZiB",
        "colab_type": "text"
      },
      "source": [
        "### sum()"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "5ZSsnwvfXb15",
        "colab_type": "code",
        "outputId": "a29660de-84d2-4a9b-e4f2-f5cf26558edc",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "print('X dizisinin tüm elemanlarının toplamı', X.sum())\n",
        "print('X dizisinin sütunlarının toplamı:', X.sum(axis=0))\n",
        "print('X dizisinin satırlarının toplamı:', X.sum(axis=1))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "X dizisinin tüm elemanlarının toplamı 10\n",
            "X dizisinin sütunlarının toplamı: [4 6]\n",
            "X dizisinin satırlarının toplamı: [3 7]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "c1ok7nNHXtq-",
        "colab_type": "text"
      },
      "source": [
        "### std()"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "sB6mZmi9X1Rv",
        "colab_type": "code",
        "outputId": "4274e688-ad12-4f92-d8cd-e8d4e4153aff",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "print('X dizisinin tüm elemanlarının standart sapması:', X.std())\n",
        "print('X dizisinin sütunlarının standart sapması:', X.std(axis=0))\n",
        "print('X dizisinin satırlarının standart sapması:', X.std(axis=1))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "X dizisinin tüm elemanlarının standart sapması: 1.118033988749895\n",
            "X dizisinin sütunlarının standart sapması: [1. 1.]\n",
            "X dizisinin satırlarının standart sapması: [0.5 0.5]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "2ScBtw2sYDAF",
        "colab_type": "text"
      },
      "source": [
        "### median()"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "nMe46T3tYFgg",
        "colab_type": "code",
        "outputId": "3fbc17a7-06b0-45fe-e945-98a987a9770f",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "print('X dizisinin tüm elemanlarının medyanı:', np.median(X))\n",
        "print('X dizisinin sütunlarının medyanı:', np.median(X,axis=0))\n",
        "print('X dizisinin satırlarının medyanı:', np.median(X,axis=1))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "X dizisinin tüm elemanlarının medyanı: 2.5\n",
            "X dizisinin sütunlarının medyanı: [2. 3.]\n",
            "X dizisinin satırlarının medyanı: [1.5 3.5]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "vxbsbEdvYXG8",
        "colab_type": "text"
      },
      "source": [
        "### max()"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "sOUDiP5fYZn1",
        "colab_type": "code",
        "outputId": "30ae6163-542b-4849-90ed-d77e611f27af",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "print('X dizisinin tüm elemanlarının içindeki maksimum elemanı:', X.max())\n",
        "print('X dizisinin sütunlarının max elemanı:', X.max(axis=0))\n",
        "print('X dizisinin satırlarının max elemanı:', X.max(axis=1))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "X dizisinin tüm elemanlarının içindeki maksimum elemanı: 4\n",
            "X dizisinin sütunlarının max elemanı: [3 4]\n",
            "X dizisinin satırlarının max elemanı: [2 4]\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "FmgYfVfGYrb_",
        "colab_type": "text"
      },
      "source": [
        "### min()"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "8XJY8sbYYs7v",
        "colab_type": "code",
        "outputId": "40e1bd9b-93ea-44e9-8ba4-2d329a07e080",
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 68
        }
      },
      "source": [
        "print('X dizisinin tüm elemanlarının içindeki minimum elemanı:', X.min())\n",
        "print('X dizisinin sütunlarının minimum elemanı:', X.min(axis=0))\n",
        "print('X dizisinin satırlarının minimum elemanı::', X.min(axis=1))"
      ],
      "execution_count": 0,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "X dizisinin tüm elemanlarının içindeki minimum elemanı: 1\n",
            "X dizisinin sütunlarının minimum elemanı: [1 2]\n",
            "X dizisinin satırlarının minimum elemanı:: [1 3]\n"
          ],
          "name": "stdout"
        }
      ]
    }
  ]
}
