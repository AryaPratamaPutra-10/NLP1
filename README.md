<h1 align="center">Creating anime characters using Deep Convolutional Generative Adversarial Networks (DCGANs) and Keras </h1>



<h2>Setup </h2>

<h3>
  <div style="display: flex; align-items: center;">
    <span>Locally (via Anaconda + Tensorflow)</span>
        <a href="https://www.anaconda.com/">
            <img src="https://skillicons.dev/icons?i=anaconda" alt="Anaconda" style="height: 24px; margin-left: 8px;">
        </a>
        <a href="https://www.tensorflow.org/install/pip">
            <img src="https://skillicons.dev/icons?i=tensorflow" alt="Tensorflow" style="height: 24px; margin-left: 8px;">
        </a>
  </div>
</h3>

<ol>

  
  <li>
    <ul>
      <li><strong>Create a New Environment</strong>
      <li>Click on the "Environments" tab on the left sidebar.</li>
      <li>Click "Create" at the bottom left.</li>
      <li>Name the environment <code>dcgan-anime</code> and choose Python version <code>3.10.x</code>.</li>
      <li>Open Anaconda Prompt</li>
      <li>Type this on your Anaconda Prompt<pre><code>conda activate dcgan-anime</code></pre></li>
      <li>Install Tensorflow first :</li>
        <ul>
           <li><pre><code>conda install tensorflow</pre></code></li>
        </ul>
        <li>Install other dependencies used in this project :</li>
        <ul>
          <li>
            <a href="https://github.com/tensorflow/tensorflow/issues/60216#:~:text=Numpy%20was%20pinned%20to%20%3C1.24%20since%20it%20affected%20few%20tests%20on%20Ragged%20Tensors.%20Agree%20that%20we%20should%20fix%20those%20tests%20and%20remove%20the%20upperbound%20in%20future%20releases.">NumPy</a></br>
            <pre><code>conda install numpy==1.21.4</pre></code>
          </li>
          <li>
            <a href="https://matplotlib.org/devdocs/devel/min_dep_policy.html#:~:text=of%20the%20dependencies.-,Matplotlib,1.23.0,-3.8">Matplotlib</a></br>
            <pre><code>conda install matplotlib==3.5.0</pre></code>
          </li>
          <li>
            <a href="https://pandas.pydata.org/pandas-docs/version/2.1.3/getting_started/install.html#:~:text=Required%20dependencies">Pandas</a></br>
            <pre><code>conda install pandas==1.3.4</pre></code>
          </li>
          <li>
            Scikit Learn</br>
            <pre><code>conda install scikit-learn</pre></code>
          </li>
          <li>
            seaborn</br>
            <pre><code>conda install seaborn=0.9.0</pre></code>
          </li>
          <li>
            IPyKernel</br>
            <pre><code>conda install ipykernel</pre></code>
          </li>
          <li>
            Skills Network</br>
            <pre><code>pip install skillsnetwork</pre></code>
          </li>
        </ul>
        <li>
            The following required libraries are not pre-installed in the Skills Network Labs environment. You will need to run the following cell to install them:</br>
            <pre><code>pip install tqdm skillsnetwork</pre></code>
          </li>
    </ul>
  </li>
</ol>
</br>
<span>Remember to use <code>dcgan-anime</code> kernel when you try to run the notebooks.</span>


</br>
Note : If you want to use TPU, copy and run this code first <pre><code>!pip install tensorflow==2.11.0 protobuf==3.19.0
</code></pre>before you jump into another line.</span>

<h2>Dokumentasi Project</h2>
<ol>
  <li><strong>Persiapan Data</strong>: Mempersiapkan dataset berupa gambar anime yang diambil dari kaggle berupa file json untuk pelatihan</li>
  <li><strong>Menggunakan Model GAN</strong>: Menggunakan 2 komponen dari GAN yaitu Generator dan Diskriminator dan menguraikan Loop training GAN</li>
  <li><strong>Arsitektur DCGAN</strong>: Menambahkan arsitektur untuk Deep Convolutional GAN, menyempurnakan GAN dengan lapisan CNN untuk meningkatkan kualitas pembuatan gambar</li>
  <li><strong>Training</strong>: Mengimplementasikan loop pelatihan menggunakan kerangka Keras, termasuk pembaruan batch, pelacakan kehilangan, dan pengambilan sampel gambar yang dihasilkan untuk masukan selama pelatihan</li>
  <li><strong>Eksplorasi Ruang Laten</strong>: Eksplorasi dengan berbagai vektor ruang laten untuk mengontrol dan menyempurnakan gaya karakter dan ekspresi yang dihasilkan oleh model</li>
</ol>

<h2>Teknologi yang Digunakan 🛠️</h2>
<ul>
<li><strong>Python</strong>: Bahasa pemrograman untuk mengimplementasikan model DCGAN dan pipeline pelatihan
<li><strong>Keras dengan TensorFlow Backend</strong>: Digunakan untuk membangun dan melatih model DCGAN, memanfaatkan kemampuan GPU TensorFlow untuk pembelajaran mendalam yang efisien.
<li><strong>NumPy</strong>: Dasar untuk menangani operasi larik dan mengelola transformasi dataset.
<li><strong>Matplotlib</strong>: Digunakan untuk memvisualisasikan gambar yang dihasilkan pada berbagai tahap pelatihan untuk melacak kemajuan dan hasil.
<li><strong>Anaconda</strong>: Menyediakan lingkungan yang terisolasi untuk mengelola ketergantungan dan versi, memastikan reproduktifitas di berbagai sistem yang berbeda.
<li><strong>Google Colab (opsional)</strong>: Menawarkan sumber daya GPU gratis untuk mempercepat pelatihan model, ideal untuk pengguna tanpa akses GPU lokal.</li> <li>
</ul>



<h2>Analisis Teknologi Yang Digunakan 🧩</h2>
<ol>
<li><strong>Keras dengan TensorFlow</strong>: Keras berfungsi untuk pembuatan model menyederhanakan pengembangan arsitektur DCGAN, dan TensorFlow memungkinkan komputasi yang dioptimalkan, terutama pada GPU.</li>
<li><strong>DCGAN</strong>: Varian GAN ini memanfaatkan lapisan konvolusi untuk meningkatkan pembuatan gambar berkualitas tinggi, sehingga cocok untuk tugas-tugas visual seperti pembuatan karakter anime.</li>
<li><strong>NumPy dan Matplotlib</strong>: Library ini memfasilitasi penanganan data dan visualisasi, yang sangat penting untuk pra-pemrosesan set data dan memantau kemajuan pelatihan GAN.</li>
<li><strong>Anaconda dan Google Colab</strong>: Penggunaan Anaconda memastikan lingkungan yang konsisten, sementara dukungan GPU Google Colab memungkinkan eksperimen yang lebih cepat tanpa memerlukan mesin lokal kelas atas, sehingga dapat diakses untuk tujuan edukasi.</li>
</ol>



<h2>Kesimpulan </h2>
<p>Proyek ini mendemonstrasikan bagaimana Deep Convolutional Generative Adversarial Networks (DCGAN) dapat digunakan untuk menghasilkan karakter anime yang unik dan berkualitas tinggi. Dengan memanfaatkan kemampuan jaringan konvolusional dalam arsitektur GAN, model ini dapat mempelajari pola dan gaya visual dari dataset karakter anime, menghasilkan gambar yang realistis dengan kualitas yang baik </p>


