import React from "react";
import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";

const suratParts = [
  "Hai Abel,\n\nSemoga kamu lagi dalam keadaan baik ya...",
  "Abel, jujur aja, belakangan ini aku sering banget mikirin kamu...",
  "Bukan kangen yang berat atau menuntut ya, tapi kangen yang hangat...",
  "Aku juga minta maaf, Bel, kalau selama ini aku pernah salah langkah...",
  "Aku tahu, kita masih di tahap awal. Bahkan mungkin buat kamu, aku belum jadi siapa-siapa...",
  "Rasa ini bukan tentang milikin, tapi tentang keinginan buat nyimpen kamu baik-baik di hati...",
  "Kalau suatu hari kamu baca ini dan senyum, itu udah cukup buat aku...",
  "Maaf sekali lagi kalau aku terlalu jujur. Tapi aku pikir, daripada terus disimpan, lebih baik aku ungkapkan...",
  "Beberapa waktu lalu, aku iseng nulis tentang momen-momen kecil...",
  "Kadang aku ngebayangin, gimana kalau suatu hari kita bisa duduk berdua...",
  "Aku tahu aku bukan yang paling menarik, paling lucu, atau paling berpengalaman...",
  "Kalau suatu hari nanti kamu ngeliat langit sore dan inget aku...",
  "Ada satu malam yang nggak bisa aku lupain. Malam yang sunyi, tapi hati aku berisik mikirin kamu...",
  "Aku tahu semua ini mungkin cuma harapan. Tapi bukankah semua yang besar dimulai dari harapan kecil?..."
];

export default function SuratKangenAbel() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-pink-100 to-purple-200 p-6 flex flex-col items-center justify-center space-y-6">
      {suratParts.map((text, index) => (
        <motion.div
          key={index}
          initial={{ opacity: 0, y: 50 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8, delay: index * 0.5 }}
          className="w-full max-w-2xl"
        >
          <Card className="bg-white/70 backdrop-blur-xl shadow-xl rounded-2xl border-none">
            <CardContent className="p-6 text-lg text-gray-800 leading-relaxed">
              {text}
            </CardContent>
          </Card>
        </motion.div>
      ))}
    </div>
  );
}
