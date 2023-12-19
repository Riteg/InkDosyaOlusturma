---


---

<h1 id="ink-dosya-oluşturma">Ink Dosya Oluşturma</h1>
<p>Her kişilik tipi için farklı bir ink dosyası oluşturulmalı. Bu dosya içinde her bir diyalog ayrı bir <strong>Divert</strong> içinde yazılmalı. Eğer bu diyaloğun bir ilişki seviyesine göre gözükmesi isteniyorsa ona bir <a href="#relation"><strong>Relation</strong></a> etiketi eklenir.</p>
<p>Diyaloğun sahip olduğu seçimlerden birisi seçildiğinde oyuncuya sipariş eklenmek isteniyorsa ona <a href="#order"><strong>Order</strong></a> etiketi atanır</p>
<h1 id="etiketler-tags">Etiketler (Tags)</h1>
<p>Önceden belirlenmiş etiketler ile diyaloğun istenen bölümüne bir görev veya koşul atanır.</p>
<h2 id="relation">Relation</h2>
<p>Geçerli diyaloğun ilişki seviyesine bağlanması için kullanılır.</p>
<ul>
<li>
<h3 id="başlangıç-ve-bitiş-aralığı-belirtmek">Başlangıç Ve Bitiş Aralığı Belirtmek</h3>
<blockquote>
<p>relation &lt;min&gt; &lt;max&gt;</p>
</blockquote>
<p>Şeklinde yazılır.</p>
<p><code>&lt;min&gt;</code> yerine kabul edilebilir en küçük ilişki değeri yazılır.<br>
<code>&lt;max&gt;</code> yerine kabul edilebilir en büyük ilişki değeri yazılır</p>
</li>
<li>
<h3 id="başlangıç-aralığı-belirtmek">Başlangıç Aralığı Belirtmek</h3>
<blockquote>
<p>relation &lt;min&gt;</p>
</blockquote>
<p>Şeklinde yazılır. Maksimum kabul edilebilir ilişki sınır yoktur.</p>
<p><code>&lt;min&gt;</code> yerine kabul edilebilir en küçük ilişki değeri yazılır.</p>
</li>
<li>
<h3 id="bitiş-aralığı-belirtmek">Bitiş Aralığı Belirtmek</h3>
<blockquote>
<p>relation $&lt;max&gt;</p>
</blockquote>
<p>Şeklinde yazılır. Minimum kabul edilebilir ilişki sınır yoktur.</p>
<p><code>&lt;max&gt;</code> yerine kabul edilebilir en büyük ilişki değeri yazılır.</p>
</li>
</ul>
<h2 id="order">Order</h2>
<p>Geçerli seçimde veya diyalogda sipariş ataması yapmak için kullanılır.</p>
<ul>
<li>
<h3 id="tek-bir-ürün-i̇le-sipariş-oluşturmak">Tek Bir Ürün İle Sipariş Oluşturmak</h3>
<blockquote>
<p>order &lt;item_name&gt; &lt;count&gt;</p>
</blockquote>
<p>Şeklinde yapılır.</p>
<p><code>&lt;item_name&gt;</code> yerine sipariş verilmesi istanilen ürünün ismi yazılır.<br>
<code>&lt;count&gt;</code> yerine sipariş verilecek üründen kaç adet sipariş verilmesi istendiği yazılır.</p>
</li>
<li>
<h3 id="birden-fazla-ürün-i̇le-sipariş-oluşturma">Birden Fazla Ürün İle Sipariş Oluşturma</h3>
<blockquote>
<p>order &lt;item_name_1&gt;,&lt;item_name_2&gt; &lt;count_1&gt;,&lt;count_2&gt;</p>
</blockquote>
<p>Şeklinde yapılır. Bu şekilde istenildiği kadar ürün içeren bir sipariş oluşturulabilir.</p>
<p><code>&lt;item_name&gt;</code> yerine sipariş verilmesi istanilen ürünün ismi yazılır.<br>
<code>&lt;count&gt;</code> yerine sipariş verilecek üründen kaç adet sipariş verilmesi istendiği yazılır.</p>
</li>
<li>
<h3 id="rastgele-ürün-i̇le-sipariş-oluşturma">Rastgele Ürün İle Sipariş Oluşturma</h3>
<blockquote>
<p>order</p>
</blockquote>
<p>veya</p>
<blockquote>
<p>order $ $</p>
</blockquote>
<p>Şeklinde yapılır. Sadece <code>order</code> etiketini kullanmak bir ürün içeren bir sipariş olşturur. Eğer <code>order</code> etiketinin yanına <code>$</code> koyulursa o siparişin kaç adet ürün içereceği belirtilmiş olur.</p>
</li>
</ul>

