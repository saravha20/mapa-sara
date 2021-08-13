# hello-world
Desenvolver uma página web estática e de forma estruturada
&lt;!DOCTYPE html&gt;
&lt;html lang=&quot;pt-BR&quot;&gt;
&lt;head&gt;
   &lt;meta charset=&quot;UTF-8&quot;&gt;
   &lt;title&gt;Atividade 1&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
   &lt;?php
   $func = array(
       1 =&gt; array(
           &#39;col&#39; =&gt; &#39;Jose&#39;,
           &#39;sal&#39; =&gt; 2000.30,
           &#39;Sem1&#39; =&gt; 1500.10,
           &#39;Sem2&#39; =&gt; 2250.00,
           &#39;Sem3&#39; =&gt; 2800.00,
           &#39;Sem4&#39; =&gt; 1900.00
       ),
       2 =&gt; array(
           &#39;col&#39; =&gt; &#39;Tadeu&#39;,
           &#39;sal&#39; =&gt; 2500.00,
           &#39;Sem1&#39; =&gt; 1500.00,
           &#39;Sem2&#39; =&gt; 4150.20,
           &#39;Sem3&#39; =&gt; 3500.00,
           &#39;Sem4&#39; =&gt; 2100.00
       ),
       3 =&gt; array(
           &#39;col&#39; =&gt; &#39;Amanda&#39;,
           &#39;sal&#39; =&gt; 1800.00,
           &#39;Sem1&#39; =&gt; 1500.00,

           &#39;Sem2&#39; =&gt; 6950.00,
           &#39;Sem3&#39; =&gt; 4800.40,
           &#39;Sem4&#39; =&gt; 2250.00
       ),
       4 =&gt; array(
           &#39;col&#39; =&gt; &#39;Tsara&#39;,
           &#39;sal&#39; =&gt; 2200.00,
           &#39;Sem1&#39; =&gt; 1500.00,
           &#39;Sem2&#39; =&gt; 4250.80,
           &#39;Sem3&#39; =&gt; 3200.00,
           &#39;Sem4&#39; =&gt; 1980.00
       )
   );
   ?&gt;
 
   &lt;table class=&quot;tabela&quot;&gt;
       &lt;thead&gt;
           &lt;tr class=&quot;color&quot;&gt;
               
               &lt;th&gt;Colaborador&lt;/th&gt;
               &lt;th&gt;Sálario Fixo&lt;/th&gt;
               &lt;th class=&quot;text-center&quot;&gt;Venda Semana 1&lt;/th&gt;
               &lt;th class=&quot;text-center &quot;&gt;Venda Semana 2&lt;/th&gt;
               &lt;th class=&quot;text-center&quot;&gt;Venda Semana 3&lt;/th&gt;
               &lt;th class=&quot;text-center&quot;&gt;Venda Semana 4&lt;/th&gt;
               &lt;th class=&quot;text-center&quot;&gt;Total Vendas&lt;/th&gt;
               &lt;th class=&quot;text-center&quot;&gt;Comissão&lt;/th&gt;
               &lt;th class=&quot;text-center&quot;&gt;Sálario Final&lt;/th&gt;
           &lt;/tr&gt;

       &lt;/thead&gt;
       &lt;tbody&gt;
           &lt;?php
           foreach ($func as $colaborador =&gt; $valor) {
               $TotalSema = $valor[&#39;Sem1&#39;] + $valor[&#39;Sem2&#39;] +
$valor[&#39;Sem3&#39;] + $valor[&#39;Sem4&#39;];
               $comissao = $TotalSema * 0.05;
               $SalFinal = $comissao + $valor[&#39;sal&#39;];
           ?&gt;
               &lt;tr&gt;
                   
                   &lt;td&gt;&lt;?php echo $valor[&#39;col&#39;]; ?&gt;&lt;/td&gt;
                   &lt;td&gt;&lt;?php echo $valor[&#39;sal&#39;]; ?&gt;&lt;/td&gt;
                   &lt;td&gt;&lt;?php echo $valor[&#39;Sem1&#39;]; ?&gt;&lt;/td&gt;
                   &lt;td&gt;&lt;?php echo $valor[&#39;Sem2&#39;]; ?&gt;&lt;/td&gt;
                   &lt;td&gt;&lt;?php echo $valor[&#39;Sem3&#39;]; ?&gt;&lt;/td&gt;
                   &lt;td&gt;&lt;?php echo $valor[&#39;Sem4&#39;]; ?&gt;&lt;/td&gt;
                   &lt;td&gt;&lt;?php echo $TotalSema; ?&gt;&lt;/td&gt;
                   &lt;td&gt;&lt;?php echo $comissao; ?&gt;&lt;/td&gt;
                   &lt;td&gt;&lt;?php echo $SalFinal; ?&gt;&lt;/td&gt;
               &lt;/tr&gt;
           &lt;?php } ?&gt;
       &lt;/tbody&gt;
   &lt;/table&gt;
&lt;/body&gt;
&lt;/html&gt;
