# madintangho
ujian berbasis online dengan sistem CBT untuk kelas aliyyah tsalis
            
            questions.forEach((q, index) => {
                const selectedOption = document.querySelector(`input[name="q${index}"]:checked`);
                if (selectedOption && parseInt(selectedOption.value) === q.answer) {
                    score++;  // Tambah skor jika jawaban benar
                }
            });
            
            // Tampilkan hasil
            const nama = document.getElementById('nama').value;
            const kode = document.getElementById('kode').value;
            resultDiv.innerHTML = `
                <div class="result">
                    <h2>Hasil Ujian</h2>
                    <p><strong>Nama:</strong> ${nama}</p>
                    <p><strong>Kode Unik:</strong> ${kode}</p>
                    <p><strong>Jumlah Jawaban Benar:</strong> ${score} dari 10</p>
                    <p>${score >= 7 ? 'Selamat, Anda lulus!' : 'Silakan coba lagi.'}</p>
                </div>
            `;
            resultDiv.classList.remove('hidden');  // Tampilkan div hasil
            quizForm.classList.add('hidden');  // Sembunyikan form quiz
            submitQuiz.classList.add('hidden');  // Sembunyikan tombol submit
        });
    </script>
</body>
</html>
