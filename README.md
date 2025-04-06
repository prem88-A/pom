import React, { useState } from "react";
import { Card, CardContent, TextField, Button } from "@material-ui/core"; // ใช้ Material UI
import { motion } from "framer-motion";

// กำหนดประเภทข้อมูลของ state
interface WeatherData {
  temp: number;
  desc: string;
}

const TrafficLoginPage: React.FC = () => {
  const [username, setUsername] = useState<string>("");
  const [password, setPassword] = useState<string>("");
  const [loggedIn, setLoggedIn] = useState<boolean>(false);
  const [weather, setWeather] = useState<WeatherData | null>(null);

  const handleLogin = () => {
    if (username === "admin" && password === "1234") {
      setLoggedIn(true);
    } else {
      alert("ชื่อผู้ใช้หรือรหัสผ่านไม่ถูกต้อง");
    }
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-blue-900 to-black flex flex-col items-center justify-center p-4 space-y-6">
      <motion.div
        initial={{ opacity: 0, y: -50 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.5 }}
      >
        <Card className="w-[380px] shadow-2xl border border-yellow-400">
          <CardContent className="space-y-6 p-6">
            <h1 className="text-2xl font-bold text-white text-center">
              ระบบจราจร ร้อยเอ็ด
            </h1>
            {!loggedIn ? (
              <>
                <TextField
                  label="ชื่อผู้ใช้"
                  value={username}
                  onChange={(e) => setUsername(e.target.value)}
                  fullWidth
                  margin="normal"
                  className="bg-gray-800 text-white"
                />
                <TextField
                  label="รหัสผ่าน"
                  type="password"
                  value={password}
                  onChange={(e) => setPassword(e.target.value)}
                  fullWidth
                  margin="normal"
                  className="bg-gray-800 text-white"
                />
                <Button
                  variant="contained"
                  color="primary"
                  className="w-full mt-4"
                  onClick={handleLogin}
                >
                  เข้าสู่ระบบ
                </Button>
              </>
            ) : (
              <div className="space-y-4 text-white">
                <Card className="bg-gray-900">
                  <CardContent>
                    <h2 className="text-lg font-semibold mb-2">แผนที่จราจร</h2>
                    <iframe
                      src="https://www.google.com/maps/embed/v1/place?key=YOUR_GOOGLE_MAPS_API_KEY&q=Roi+Et+Thailand"
                      width="100%"
                      height="200"
                      style={{ border: 0 }}
                      allowFullScreen
                      loading="lazy"
                    ></iframe>
                  </CardContent>
                </Card>
                <Card className="bg-gray-900">
                  <CardContent>
                    <h2 className="text-lg font-semibold mb-2">ข่าวจราจร</h2>
                    <ul className="list-disc list-inside">
                      <li>หลีกเลี่ยงถนนแจ้งสนิท ช่วงเย็น – รถติด</li>
                      <li>แนะนำเส้นทางผ่านบ้านป่าไม้</li>
                    </ul>
                  </CardContent>
                </Card>
                <Card className="bg-gray-900">
                  <CardContent>
                    <h2 className="text-lg font-semibold mb-2">ฟังวิทยุจราจร</h2>
                    <audio controls className="w-full">
                      <source
                        src="https://radio.streaming.in.th:8443/fm91.mp3"
                        type="audio/mpeg"
                      />
                      เบราว์เซอร์ของคุณไม่รองรับการเล่นเสียง
                    </audio>
                  </CardContent>
                </Card>
              </div>
            )}
          </CardContent>
        </Card>
      </motion.div>
    </div>
  );
}

export default TrafficLoginPage;
