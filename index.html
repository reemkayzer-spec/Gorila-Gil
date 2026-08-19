<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>תפעול והדרכה - צוות גיל</title>
    
    <!-- Chart.js לסרגל נתונים ודשבורד אינטראקטיבי -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

    <!-- Supabase SDK -->
    <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

    <!-- Firebase SDKs & Email/Password Auth Integration -->
    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
        import { getAuth, signInWithEmailAndPassword, onAuthStateChanged, signOut, setPersistence, browserLocalPersistence } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-auth.js";
        import { getDatabase, ref, set, onValue, get, update, push, remove } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-database.js";

        const firebaseConfig = {
            apiKey: "AIzaSyCdqf9bo_mMiMxjXU24zMnrDgX4qTLcHwM",
            authDomain: "gorilla-training.firebaseapp.com",
            databaseURL: "https://gorilla-training-default-rtdb.firebaseio.com",
            projectId: "gorilla-training",
            storageBucket: "gorilla-training.firebasestorage.app",
            messagingSenderId: "407883236078",
            appId: "1:407883236078:web:6473279dba7520a32fa9ff",
            measurementId: "G-9LZQPRKYNT"
        };

        const app = initializeApp(firebaseConfig);
        const auth = getAuth(app);
        const db = getDatabase(app);

        window.fbDB = db;
        window.fbRef = ref;
        window.fbSet = set;
        window.fbPush = push;
        window.fbRemove = remove;
        window.fbUpdate = update;
        window.fbOnValue = onValue;
        window.fbGet = get;

        setPersistence(auth, browserLocalPersistence).catch(console.error);

        window.trainerGorillaMap = {
            "איתי הקר": ["גורילה 3", "גורילה 7"],
            "עדיאל קסה": ["גורילה 1", "גורילה 5"]
        };

        window.knownTrainers = {
            "itayhaker19@gmail.com": { firstName: "איתי", lastName: "הקר", phone: "" },
            "adielkassa@gmail.com": { firstName: "עדיאל", lastName: "קסה", phone: "0526652209" },
            "reemkayzer@gmail.com": { firstName: "ראם", lastName: "קייזר", phone: "" },
            "nadavyichye@gmail.com": { firstName: "נדב", lastName: "יחיא", phone: "" },
            "idolevko2@gmail.com": { firstName: "עידו", lastName: "לבקוביץ", phone: "" },
            "tomerk2001@gmail.com": { firstName: "תומר", lastName: "כחלון", phone: "" },
            "netashatzberg@gmail.com": { firstName: "נטע", lastName: "שצברג", phone: "" },
            "antonicbc@gmail.com": { firstName: "מרקו", lastName: "", phone: "" }
        };

        window.selectQuickTrainer = function(email) {
            const emailInput = document.getElementById("auth-email");
            const passInput = document.getElementById("auth-pass");
            if (emailInput) {
                emailInput.value = email;
                if (passInput) passInput.focus();
            }
        };

        window.loginWithCredentials = function(e) {
            if (e) e.preventDefault();
            const emailInput = document.getElementById("auth-email");
            const passInput = document.getElementById("auth-pass");
            const errEl = document.getElementById("error-msg");
            const btn = document.getElementById("loginBtn");

            const email = emailInput ? emailInput.value.trim() : "";
            const pass = passInput ? passInput.value : "";

            if (!email || !pass) {
                if (errEl) errEl.innerText = "נא להזין כתובת אימייל וסיסמה.";
                return;
            }

            if (errEl) errEl.innerText = "מתחבר...";
            if (btn) btn.disabled = true;

            signInWithEmailAndPassword(auth, email, pass)
                .then(() => {
                    localStorage.setItem('gorilla_last_email', email);
                })
                .catch((error) => {
                    if (btn) btn.disabled = false;
                    if (!errEl) return;
                    if (error.code === 'auth/invalid-credential' || error.code === 'auth/user-not-found' || error.code === 'auth/wrong-password') {
                        errEl.innerText = "שגיאה: אימייל או סיסמה אינם נכונים.";
                    } else if (error.code === 'auth/too-many-requests') {
                        errEl.innerText = "נחסמת זמנית עקב ריבוי נסיונות כושלים. נסה שוב מאוחר יותר.";
                    } else {
                        errEl.innerText = "שגיאה בהתחברות: " + error.message;
                    }
                });
        };

        window.logout = function() {
            localStorage.removeItem('gorilla_trainer_profile');
            signOut(auth);
        };

        onAuthStateChanged(auth, (user) => {
            const authScreen = document.getElementById("auth-screen");
            const mainContent = document.getElementById("main-content");
            const errEl = document.getElementById("error-msg");
            const btn = document.getElementById("loginBtn");
            const emailInput = document.getElementById("auth-email");

            if (btn) btn.disabled = false;

            if (user) {
                if (authScreen) authScreen.style.display = "none";
                if (mainContent) mainContent.style.display = "block";
                
                if (typeof window.initTrainerProfile === 'function') {
                    window.initTrainerProfile(user);
                }
                
                window.dispatchEvent(new Event('firebase-ready'));
            } else {
                if (authScreen) authScreen.style.display = "flex";
                if (mainContent) mainContent.style.display = "none";
                if (errEl) errEl.innerText = "";

                const savedEmail = localStorage.getItem('gorilla_last_email');
                if (savedEmail && emailInput && !emailInput.value) {
                    emailInput.value = savedEmail;
                }
            }
        });
    </script>

    <script>
        const SUPABASE_URL = 'https://pvtswscsqnymbbzgsafu.supabase.co';
        const SUPABASE_KEY = 'sb_publishable_wlsjLYqz458Ud69TrPR7AA_LB9xvimg';
        window.supabaseClient = supabase.createClient(SUPABASE_URL, SUPABASE_KEY);
    </script>

    <style>
        :root {
            --bg-color: #f4f6f9;
            --main-bg: #ffffff;
            --text-color: #2c3e50;
            --header-bg: #1a252f;
            --card-bg: #f8fafc;
            --border-color: #e2e8f0;
            --input-bg: #ffffff;
            --table-even: #f8fafc;
            --th-bg: #334155;
            --code-bg: #f1f5f9;
            --link-color: #3498db;
        }

        body.dark-mode {
            --bg-color: #0b0f19;
            --main-bg: #1e293b;
            --text-color: #f8fafc;
            --header-bg: #0f172a;
            --card-bg: #1e293b;
            --border-color: #334155;
            --input-bg: #0f172a;
            --table-even: #172033;
            --th-bg: #0f172a;
            --code-bg: #0f172a;
            --link-color: #58a6ff;
        }

        * { box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; -webkit-tap-highlight-color: transparent; }
        body { margin: 0; padding: 0; background-color: var(--bg-color); color: var(--text-color); line-height: 1.6; overflow-x: hidden; transition: background 0.3s, color 0.3s; }
        
        /* אפקט קפיצה אלסטי בריחוף על כלל הכפתורים והכרטיסים */
        button, .btn, .link-table-btn, .tab-btn, .week-tab-btn, .month-folder-btn, 
        .wa-group-btn, .call-btn, .unit-wa-btn, .unit-add-btn, .theme-toggle-btn, 
        .logout-btn, .trainer-save-btn, .cleaning-today-btn, .copy-btn, .yt-link-btn, .login-btn, .trainer-chip-btn, .todo-add-btn, .todo-edit-btn {
            transition: transform 0.2s cubic-bezier(0.34, 1.56, 0.64, 1), box-shadow 0.2s ease, background-color 0.2s ease, color 0.2s ease !important;
        }
        button:hover, .btn:hover, .link-table-btn:hover, .tab-btn:hover, .week-tab-btn:hover,
        .wa-group-btn:hover, .call-btn:hover, .unit-wa-btn:hover, .unit-add-btn:hover, 
        .theme-toggle-btn:hover, .logout-btn:hover, .trainer-save-btn:hover, 
        .cleaning-today-btn:hover, .copy-btn:hover, .yt-link-btn:hover, .login-btn:hover, .trainer-chip-btn:hover, .todo-add-btn:hover, .todo-edit-btn:hover {
            transform: translateY(-2.5px);
            box-shadow: 0 4px 12px rgba(0,0,0,0.18);
        }
        button:active, .btn:active, .link-table-btn:active, .tab-btn:active, .week-tab-btn:active {
            transform: translateY(0);
        }

        #auth-screen {
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            height: 100vh; background-color: #0f172a; color: #ffffff; position: fixed;
            top: 0; left: 0; width: 100%; z-index: 99999; padding: 20px;
        }
        .login-card {
            background: #1e293b; border: 1px solid #334155; border-radius: 12px;
            padding: 26px 22px; width: 100%; max-width: 390px; text-align: center; box-shadow: 0 10px 25px rgba(0,0,0,0.5);
        }
        .login-card h2 { margin: 0 0 8px 0; font-size: 1.3em; }
        .login-card p { font-size: 0.85em; color: #94a3b8; margin-bottom: 15px; }

        .quick-trainers-wrapper {
            margin-bottom: 15px;
            padding: 10px;
            background: rgba(15, 23, 42, 0.6);
            border-radius: 8px;
            border: 1px solid #334155;
        }
        .quick-trainers-title {
            font-size: 0.76em;
            color: #94a3b8;
            margin-bottom: 8px;
            font-weight: bold;
        }
        .quick-trainers-chips {
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
            justify-content: center;
        }
        .trainer-chip-btn {
            background: #334155;
            color: #f8fafc;
            border: 1px solid #475569;
            padding: 4px 10px;
            border-radius: 14px;
            font-size: 0.78em;
            font-weight: bold;
            cursor: pointer;
        }
        .trainer-chip-btn:hover {
            background: #0284c7;
            border-color: #38bdf8;
            color: white;
        }

        .login-input {
            width: 100%; padding: 12px 14px; margin-bottom: 12px; border: 1px solid #475569;
            border-radius: 8px; background: #0f172a; color: #ffffff; font-size: 0.95em; outline: none;
            direction: ltr; text-align: right; transition: 0.2s;
        }
        .login-input:focus { border-color: #38bdf8; }
        .login-btn {
            background-color: #0284c7; color: white; border: none; width: 100%; padding: 12px;
            font-size: 1em; border-radius: 8px; cursor: pointer; font-weight: bold; margin-top: 5px;
        }
        .login-btn:hover { background-color: #0369a1; }
        .login-btn:disabled { opacity: 0.6; cursor: not-allowed; }
        #error-msg { color: #f87171; font-size: 0.85em; margin-top: 12px; min-height: 18px; font-weight: bold; }

        #main-content { display: none; }

        /* באנר תזכורת למשימות המדריך */
        .todo-user-reminder-banner {
            display: none;
            max-width: 1400px;
            margin: 10px auto 0 auto;
            padding: 10px 16px;
            background: linear-gradient(90deg, #0284c7, #0369a1);
            color: white;
            border-radius: 8px;
            font-size: 0.9em;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(2, 132, 199, 0.3);
            border: 1px solid #38bdf8;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
            transition: transform 0.2s ease;
        }
        .todo-user-reminder-banner:hover { transform: translateY(-2px); }

        header { background-color: var(--header-bg); color: white; padding: 12px 8px; text-align: center; position: sticky; top: 0; z-index: 999; box-shadow: 0 4px 12px rgba(0,0,0,0.15); }
        .header-top { display: flex; justify-content: space-between; align-items: center; max-width: 1400px; margin: 0 auto 8px auto; padding: 0 6px; }
        header h1 { margin: 0; font-size: 1.15em; font-weight: 700; display: flex; align-items: center; gap: 12px; justify-content: center; }
        
        .header-actions-left { display: flex; gap: 8px; align-items: center; }
        .theme-toggle-btn, .logout-btn { background: #334155; color: white; border: none; padding: 6px 12px; border-radius: 15px; cursor: pointer; font-size: 0.78em; font-weight: bold; }
        .theme-toggle-btn:hover { background: #475569; }
        .logout-btn { background-color: #e74c3c; }
        .logout-btn:hover { background-color: #c0392b; }

        .nav-tabs { display: flex; justify-content: center; gap: 6px; flex-wrap: nowrap; overflow-x: auto; padding-bottom: 4px; -webkit-overflow-scrolling: touch; scrollbar-width: none; }
        .nav-tabs::-webkit-scrollbar { display: none; }
        .tab-btn {
            background-color: #34495e; color: white; border: none; padding: 8px 14px;
            border-radius: 6px; cursor: pointer; font-weight: bold; font-size: 0.85em; white-space: nowrap; flex-shrink: 0;
        }
        .tab-btn:hover, .tab-btn.active { background-color: #3498db; }

        main { max-width: 1400px; margin: 12px auto; padding: 16px; background: var(--main-bg); border-radius: 10px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); transition: background 0.3s; }
        .tab-content { display: none; }
        .tab-content.active { display: block; }

        /* עיצובי דשבורד */
        .dashboard-header { margin-bottom: 20px; }
        .dashboard-header h2 { margin: 0 0 4px 0; font-size: 1.3em; display: flex; align-items: center; gap: 8px; }
        .dashboard-header p { margin: 0; font-size: 0.85em; color: #64748b; }

        .dashboard-kpi-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 20px;
        }
        .kpi-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 16px;
            text-align: center;
            box-shadow: 0 2px 8px rgba(0,0,0,0.02);
            transition: transform 0.2s cubic-bezier(0.34, 1.56, 0.64, 1), box-shadow 0.2s ease;
        }
        .kpi-card:hover { 
            transform: translateY(-3px); 
            box-shadow: 0 6px 16px rgba(0,0,0,0.1);
        }
        .kpi-value { font-size: 1.9em; font-weight: 800; line-height: 1.1; margin-bottom: 4px; }
        .kpi-title { font-size: 0.85em; font-weight: 600; color: #64748b; }

        .dashboard-main-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 20px;
            margin-bottom: 20px;
        }
        @media (min-width: 900px) {
            .dashboard-main-grid {
                grid-template-columns: 1.1fr 0.9fr;
            }
        }

        .dashboard-box {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 16px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.02);
        }
        .dashboard-box-title {
            margin: 0 0 15px 0;
            font-size: 1.05em;
            font-weight: 700;
            border-bottom: 2px solid var(--border-color);
            padding-bottom: 8px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .stats-items-list { display: flex; flex-direction: column; gap: 12px; }
        .stat-item-row {
            display: flex; justify-content: space-between; align-items: center;
            background: var(--main-bg); padding: 10px 14px; border-radius: 8px; border: 1px solid var(--border-color);
            transition: transform 0.2s ease;
        }
        .stat-item-row:hover { transform: translateX(-3px); }
        .stat-item-label { font-size: 0.9em; font-weight: 600; }
        .stat-item-value { font-size: 1.1em; font-weight: 800; color: #0284c7; }

        .badges-wrap { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 6px; }
        .info-tag {
            background: rgba(2, 132, 199, 0.1); color: #0284c7; border: 1px solid rgba(2, 132, 199, 0.2);
            padding: 3px 8px; border-radius: 12px; font-size: 0.78em; font-weight: bold;
            transition: transform 0.2s ease;
        }
        .info-tag:hover { transform: translateY(-1.5px); }
        body.dark-mode .info-tag { background: rgba(56, 189, 248, 0.15); color: #38bdf8; border-color: rgba(56, 189, 248, 0.3); }

        .faults-section {
            background: var(--card-bg); border: 1px solid var(--border-color); border-right: 4px solid #ef4444;
            border-radius: 10px; padding: 16px; margin-bottom: 20px;
        }
        .fault-row-item {
            background: #fee2e2; color: #991b1b; border: 1px solid #f87171; padding: 10px 14px;
            border-radius: 8px; margin-bottom: 8px; display: flex; justify-content: space-between; align-items: center;
            font-size: 0.9em; font-weight: 600; transition: transform 0.2s ease;
        }
        .fault-row-item:hover { transform: translateX(-3px); }
        body.dark-mode .fault-row-item { background: rgba(239, 68, 68, 0.2); color: #fca5a5; border-color: #ef4444; }

        /* ================= סגנונות מודול To-Do ================= */
        .todo-container {
            max-width: 900px;
            margin: 0 auto;
        }
        .todo-header-box {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 16px;
            flex-wrap: wrap;
            gap: 10px;
        }
        .todo-header-box h2 {
            margin: 0;
            font-size: 1.4em;
            display: flex;
            align-items: center;
            gap: 10px;
            color: #38bdf8;
        }
        .todo-add-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 14px;
            margin-bottom: 20px;
            display: flex;
            flex-direction: column;
            gap: 10px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.03);
        }
        .todo-inputs-row {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
        }
        .todo-input-title {
            flex: 2;
            min-width: 220px;
            padding: 10px 14px;
            border: 1px solid var(--border-color);
            border-radius: 8px;
            background: var(--input-bg);
            color: var(--text-color);
            font-size: 0.95em;
            outline: none;
        }
        .todo-input-title:focus { border-color: #38bdf8; }
        .todo-select-assignee, .todo-input-date {
            flex: 1;
            min-width: 140px;
            padding: 10px 12px;
            border: 1px solid var(--border-color);
            border-radius: 8px;
            background: var(--input-bg);
            color: var(--text-color);
            font-size: 0.9em;
            outline: none;
            cursor: pointer;
        }
        .todo-add-btn {
            background: #0284c7;
            color: white;
            border: none;
            padding: 10px 18px;
            border-radius: 8px;
            font-weight: bold;
            font-size: 0.95em;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            justify-content: center;
        }
        .todo-add-btn:hover { background: #0369a1; }

        .todo-list-wrap {
            display: flex;
            flex-direction: column;
            gap: 8px;
            margin-bottom: 25px;
        }
        .todo-item-card {
            background: #1e293b;
            color: #f8fafc;
            border: 1px solid #334155;
            border-radius: 8px;
            padding: 12px 16px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.15);
            transition: background 0.2s, transform 0.2s ease, border-color 0.2s ease;
        }
        body:not(.dark-mode) .todo-item-card {
            background: #ffffff;
            color: #1e293b;
            border-color: #cbd5e1;
            box-shadow: 0 2px 6px rgba(0,0,0,0.04);
        }
        .todo-item-card:hover { transform: translateY(-2px); }
        
        /* צביעת שורה שלמה בצהוב כאשר המשימה מסומנת בכוכב */
        .todo-item-card.starred {
            background-color: #fef9c3 !important;
            border-color: #facc15 !important;
            color: #854d0e !important;
        }
        body.dark-mode .todo-item-card.starred {
            background-color: rgba(234, 179, 8, 0.2) !important;
            border-color: #ca8a04 !important;
            color: #fef08a !important;
        }
        .todo-item-card.starred .todo-item-title {
            color: #854d0e !important;
        }
        body.dark-mode .todo-item-card.starred .todo-item-title {
            color: #fef08a !important;
        }

        .todo-item-card.completed {
            opacity: 0.6;
        }
        .todo-item-card.completed .todo-item-title {
            text-decoration: line-through;
            color: #94a3b8 !important;
        }
        .todo-main-content {
            display: flex;
            align-items: center;
            gap: 12px;
            flex: 1;
        }
        .todo-check-btn {
            width: 22px;
            height: 22px;
            border-radius: 50%;
            border: 2px solid #64748b;
            background: transparent;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            padding: 0;
            transition: 0.2s;
        }
        .todo-check-btn.checked {
            background: #22c55e;
            border-color: #22c55e;
            color: white;
        }
        .todo-item-info {
            display: flex;
            flex-direction: column;
            gap: 2px;
        }
        .todo-item-title {
            font-size: 0.98em;
            font-weight: 600;
        }
        .todo-item-date {
            font-size: 0.78em;
            color: #94a3b8;
            display: flex;
            align-items: center;
            gap: 4px;
        }
        /* תאריך באיחור עם סימן קריאה אדום */
        .todo-item-date.overdue {
            color: #ef4444 !important;
            font-weight: 800;
        }
        .todo-item-date.due-today {
            color: #f59e0b !important;
            font-weight: bold;
        }
        .todo-item-date.due-tomorrow {
            color: #38bdf8 !important;
            font-weight: bold;
        }

        .todo-actions-right {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .trainer-badge-avatar {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 0.78em;
            flex-shrink: 0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        .todo-star-btn, .todo-edit-btn, .todo-delete-btn {
            background: none;
            border: none;
            cursor: pointer;
            padding: 4px;
            font-size: 1.1em;
            line-height: 1;
        }
        .todo-star-btn { color: #64748b; }
        .todo-star-btn.starred { color: #eab308; }
        .todo-edit-btn { color: #94a3b8; }
        .todo-edit-btn:hover { color: #38bdf8; }
        .todo-delete-btn { color: #94a3b8; }
        .todo-delete-btn:hover { color: #ef4444; }

        /* סגנונות כלליים */
        .trainer-profile-bar {
            background: var(--card-bg); border: 1px solid var(--border-color); border-radius: 8px;
            padding: 12px 16px; margin-bottom: 15px; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px;
        }
        .trainer-info-text { font-size: 0.9em; font-weight: bold; }
        .trainer-inputs-group { display: flex; gap: 8px; align-items: center; flex-wrap: wrap; }
        .trainer-inputs-group input {
            padding: 6px 10px; border: 1px solid var(--border-color); border-radius: 6px; font-size: 0.85em; background: var(--input-bg); color: var(--text-color);
        }
        .trainer-save-btn { background: #0284c7; color: white; border: none; padding: 6px 12px; border-radius: 6px; font-weight: bold; cursor: pointer; font-size: 0.85em; }
        .trainer-save-btn:hover { background: #0369a1; }

        .schedule-header-action {
            display: flex; flex-direction: column; gap: 12px; margin-bottom: 15px; background: var(--card-bg);
            padding: 12px; border-radius: 8px; border: 1px solid var(--border-color);
        }
        .action-btns-group { display: flex; gap: 8px; flex-wrap: wrap; width: 100%; }
        .action-btns-group button { flex: 1; min-width: 220px; justify-content: center; }
        
        .wa-group-btn, .call-btn {
            color: white; border: none; padding: 10px 14px;
            border-radius: 20px; font-weight: bold; cursor: pointer; font-size: 0.82em;
            display: flex; align-items: center; justify-content: center; gap: 6px; box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            text-decoration: none;
        }
        .wa-group-btn { background-color: #128c7e; }
        .wa-group-btn:hover { background-color: #0e6f64; }
        .call-btn { background-color: #27ae60; }
        .call-btn:hover { background-color: #219653; }

        .search-box { width: 100%; }
        .search-box input {
            width: 100%; padding: 10px 14px; border: 2px solid var(--border-color);
            border-radius: 25px; font-size: 0.95em; outline: none; transition: 0.3s; background: var(--input-bg); color: var(--text-color);
        }
        .search-box input:focus { border-color: #3498db; }

        .week-tabs-bar { display: flex; gap: 6px; justify-content: center; margin-bottom: 15px; flex-wrap: wrap; }
        .week-tab-btn {
            background-color: var(--card-bg); color: var(--text-color); border: 1px solid var(--border-color);
            padding: 6px 14px; border-radius: 20px; font-weight: bold; font-size: 0.85em; cursor: pointer;
        }
        .week-tab-btn:hover, .week-tab-btn.active { background-color: #0284c7; color: white; border-color: #0284c7; }
        .week-tab-btn.today-week-tab {
            background-color: #fef08a !important; color: #854d0e !important; border-color: #facc15 !important;
            font-weight: 800; box-shadow: 0 2px 8px rgba(250, 204, 21, 0.4);
        }
        body.dark-mode .week-tab-btn.today-week-tab { background-color: #713f12 !important; color: #fef08a !important; border-color: #ca8a04 !important; }

        .spreadsheet-container { display: grid; grid-template-columns: 1fr; gap: 20px; width: 100%; }
        .sheet-box { background: var(--main-bg); border-radius: 8px; border: 1px solid var(--border-color); overflow: hidden; box-shadow: 0 2px 8px rgba(0,0,0,0.02); }
        .sheet-side-header {
            background-color: #1e293b; color: white; padding: 10px 14px;
            display: flex; justify-content: space-between; align-items: center; font-size: 0.95em; font-weight: bold; flex-wrap: wrap; gap: 8px;
        }
        .header-btns-group { display: flex; gap: 6px; align-items: center; flex-wrap: wrap; }
        .unit-wa-btn, .unit-add-btn {
            color: white; border: none; padding: 5px 10px; border-radius: 20px; font-size: 0.78em; font-weight: bold; cursor: pointer;
            display: inline-flex; align-items: center; gap: 5px; box-shadow: 0 2px 5px rgba(0,0,0,0.15); white-space: nowrap;
        }
        .unit-wa-btn { background-color: #25d366; }
        .unit-wa-btn:hover { background-color: #20ba5a; }
        .unit-wa-btn svg { width: 14px; height: 14px; fill: white; flex-shrink: 0; }
        .unit-add-btn { background-color: #0284c7; }
        .unit-add-btn:hover { background-color: #0369a1; }

        .table-container { overflow-x: auto; margin: 0; border: none; border-radius: 0; -webkit-overflow-scrolling: touch; }
        .status-table-container { overflow-x: auto; width: 100%; -webkit-overflow-scrolling: touch; }
        .status-table-container table { width: 100%; min-width: 600px; }

        .status-table-container th:nth-child(1), .status-table-container td:nth-child(1) { width: 110px; min-width: 110px; } 
        .status-table-container th:nth-child(2), .status-table-container td:nth-child(2) { width: 90px; min-width: 90px; }   
        .status-table-container th:nth-child(3), .status-table-container td:nth-child(3) { width: 125px; min-width: 125px; } 
        .status-table-container th:nth-child(4), .status-table-container td:nth-child(4) { width: auto; }                    

        table { width: 100%; border-collapse: collapse; font-size: 0.78em; text-align: center; table-layout: auto; }
        th, td { border: 1px solid var(--border-color); padding: 6px 3px; vertical-align: middle; }
        th { background-color: var(--th-bg); color: white; font-weight: 600; white-space: nowrap; font-size: 0.82em; }

        .spreadsheet-container table th:nth-child(1), .spreadsheet-container table td:nth-child(1) { width: 75px; min-width: 75px; } 
        .spreadsheet-container table th:nth-child(2), .spreadsheet-container table td:nth-child(2) { width: 125px; min-width: 125px; } 
        .spreadsheet-container table th:nth-child(3), .spreadsheet-container table td:nth-child(3) { width: 50px; min-width: 50px; } 
        .spreadsheet-container table th:nth-child(4), .spreadsheet-container table td:nth-child(4) { width: 50px; min-width: 50px; } 
        .spreadsheet-container table th:nth-child(5), .spreadsheet-container table td:nth-child(5) { width: 65px; min-width: 65px; } 
        .spreadsheet-container table th:nth-child(6), .spreadsheet-container table td:nth-child(6) { width: 130px; min-width: 130px; } 
        .spreadsheet-container table th:nth-child(7), .spreadsheet-container table td:nth-child(7) { width: 40px; min-width: 40px; } 
        .spreadsheet-container table th:nth-child(8), .spreadsheet-container table td:nth-child(8) { width: 100px; min-width: 100px; } 
        .spreadsheet-container table th:nth-child(9), .spreadsheet-container table td:nth-child(9) { width: 50px; min-width: 50px; } 
        .spreadsheet-container table th:nth-child(10), .spreadsheet-container table td:nth-child(10) { width: 110px; min-width: 110px; } 
        .spreadsheet-container table th:nth-child(11), .spreadsheet-container table td:nth-child(11) { width: 90px; min-width: 90px; } 
        
        .today-row td { background-color: #fef08a !important; border-color: #facc15 !important; font-weight: bold; }
        body.dark-mode .today-row td { background-color: #713f12 !important; border-color: #fef08a !important; }

        .canceled-row td { background-color: rgba(239, 68, 68, 0.2) !important; border-color: #f87171 !important; }
        body.dark-mode .canceled-row td { background-color: rgba(239, 68, 68, 0.3) !important; border-color: #991b1b !important; }

        .cell-input { width: 100%; border: none; background: transparent; text-align: center; font-size: 0.88em; color: var(--text-color); outline: none; padding: 2px; }
        .cell-input:focus { background: rgba(52, 152, 219, 0.1); border-radius: 4px; }

        .cell-select {
            width: 100%; border: 1px solid var(--border-color); background: var(--input-bg);
            color: var(--text-color); font-size: 0.78em; border-radius: 4px; padding: 2px 1px; outline: none; cursor: pointer;
        }
        .cell-select.has-selection { appearance: none; -webkit-appearance: none; background: transparent; border: none; text-align-last: center; font-weight: bold; }

        .guides-container, .gorillas-container { display: flex; flex-direction: column; gap: 3px; width: 100%; }
        .guide-row-flex, .gorilla-row-flex { display: flex; align-items: center; gap: 2px; width: 100%; }
        .add-guide-btn, .remove-guide-btn, .add-gorilla-btn, .remove-gorilla-btn {
            background: none; border: none; cursor: pointer; font-size: 0.85em; padding: 0 2px; line-height: 1; flex-shrink: 0;
        }
        .add-guide-btn:hover, .remove-guide-btn:hover, .add-gorilla-btn:hover, .remove-gorilla-btn:hover { transform: scale(1.25) translateY(-1px); }

        .month-folders-bar {
            display: flex; gap: 6px; overflow-x: auto; padding: 14px 6px; margin-top: 20px;
            border-top: 2px solid var(--border-color); background: var(--card-bg); border-radius: 8px; justify-content: center; flex-wrap: wrap; align-items: flex-end;
        }
        .month-folder-btn {
            background-color: #475569; color: white; border: none; padding: 9px 16px; border-radius: 6px 6px 0 0; cursor: pointer; font-weight: bold; font-size: 0.9em;
        }
        .month-folder-btn:hover { background-color: #64748b; transform: translateY(-4px); }
        .month-folder-btn.active {
            background-color: #0284c7; color: #ffffff; transform: translateY(-6px) scale(1.08);
            box-shadow: 0 6px 16px rgba(2, 132, 199, 0.5); border: 2px solid #ffffff; font-weight: 800; z-index: 10;
        }

        .status-select, .notes-input {
            padding: 5px 10px; border-radius: 6px; border: 1px solid var(--border-color);
            background-color: var(--input-bg); color: var(--text-color); font-size: 0.9em; font-weight: bold; outline: none; transition: 0.2s;
        }
        .status-select { cursor: pointer; }
        .notes-input { width: 100%; }
        .status-select:focus, .notes-input:focus { border-color: #3498db; }

        .cleaning-date-wrapper { display: flex; align-items: center; gap: 6px; justify-content: center; flex-wrap: wrap; }
        .cleaning-date-input { padding: 3px 6px; border-radius: 4px; border: 1px solid var(--border-color); background: var(--input-bg); color: var(--text-color); font-size: 0.85em; outline: none; }
        .cleaning-today-btn {
            background-color: #25d366; color: white; border: none; padding: 4px 10px; border-radius: 15px;
            font-size: 0.78em; font-weight: bold; cursor: pointer; white-space: nowrap; box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .cleaning-today-btn:hover { background-color: #20ba5a; }

        .slide-box {
            background-color: var(--card-bg); border: 1px solid var(--border-color); border-right: 4px solid #3498db;
            border-radius: 8px; margin-bottom: 15px; padding: 12px; box-shadow: 0 2px 5px rgba(0,0,0,0.02); transition: background 0.3s, border-color 0.3s;
        }
        .slide-title { margin-top: 0; color: var(--text-color); border-bottom: 2px solid var(--border-color); padding-bottom: 6px; font-size: 1.05em; }
        .step-list { margin-top: 8px; padding-right: 12px; font-size: 0.9em; }
        .step-list li { margin-bottom: 8px; }
        .step-list p { margin: 4px 0; }
        .code-block { background: var(--code-bg); padding: 2px 5px; border-radius: 4px; font-family: monospace; direction: ltr; display: inline-block; color: var(--text-color); border: 1px solid var(--border-color); font-size: 0.85em; word-break: break-all; }

        .videos-flex-container { display: flex; gap: 10px; flex-direction: column; margin: 12px 0; }
        @media (min-width: 768px) { .videos-flex-container { flex-direction: row; flex-wrap: wrap; } }
        .slide-video-container { background: var(--card-bg); border: 1px solid var(--border-color); border-radius: 8px; padding: 10px; flex: 1; width: 100%; }
        .slide-video-container h4 { margin: 0 0 6px 0; font-size: 0.85em; color: var(--text-color); }
        .video-wrapper { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 6px; background: #000; }
        .video-wrapper iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0; }
        .yt-link-btn {
            display: inline-flex; align-items: center; gap: 6px; background-color: #ff0000; color: white;
            padding: 6px 10px; border-radius: 15px; text-decoration: none; font-size: 0.78em; font-weight: bold; margin-top: 6px;
        }

        .cards-container { display: flex; gap: 10px; flex-direction: column; margin-top: 10px; }
        @media (min-width: 600px) { .cards-container { flex-direction: row; flex-wrap: wrap; } }
        .card { background: var(--card-bg); border: 1px solid var(--border-color); border-radius: 8px; padding: 12px; flex: 1; min-width: 280px; }
        .form-card-content { display: flex; justify-content: space-between; align-items: center; gap: 12px; flex-wrap: wrap; }
        .form-info { flex: 1; min-width: 160px; }
        .form-qr-box { display: flex; flex-direction: column; align-items: center; background: var(--main-bg); padding: 8px; border-radius: 6px; border: 1px solid var(--border-color); text-align: center; }
        .form-qr-box img { width: 90px; height: 90px; border-radius: 4px; background: white; padding: 3px; margin-bottom: 4px; }
        .form-url-text { font-size: 0.7em; direction: ltr; color: var(--text-color); max-width: 110px; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; margin-bottom: 4px; }
        .copy-btn { background-color: #64748b; color: white; border: none; padding: 3px 8px; border-radius: 4px; font-size: 0.72em; cursor: pointer; font-weight: bold; }
        .copy-btn:hover { background-color: #475569; }

        .btn { display: inline-block; background-color: #0284c7; color: white; padding: 8px 12px; text-decoration: none; border-radius: 6px; font-weight: bold; margin-top: 6px; font-size: 0.85em; text-align: center; width: 100%; }
        @media (min-width: 600px) { .btn { width: auto; } }

        .link-table-btn { display: inline-block; background-color: #0284c7; color: white; padding: 6px 10px; border-radius: 4px; text-decoration: none; font-weight: bold; font-size: 0.8em; text-align: center; }
        .table-title { background-color: #1e293b; color: white; padding: 10px 12px; border-radius: 8px 8px 0 0; margin-top: 15px; margin-bottom: 0; font-size: 1em; display: flex; justify-content: space-between; align-items: center; }
        .slide-img-box { text-align: center; margin: 12px 0; }
        .slide-img-box img { max-width: 100%; height: auto; border-radius: 8px; border: 1px solid var(--border-color); box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
    </style>
</head>
<body>

    <!-- מסך התחברות מהיר וידידותי -->
    <div id="auth-screen">
        <form class="login-card" onsubmit="loginWithCredentials(event)" autocomplete="on">
            <div style="display:inline-flex; align-items:center; justify-content:center; width:44px; height:44px; background:#f37021; border-radius:10px; margin-bottom:10px;">
                <svg width="28" height="28" viewBox="0 0 100 100" style="transform: rotate(-45deg);">
                    <rect x="35" y="20" width="30" height="60" rx="15" fill="#1e293b"/>
                    <path d="M 35 35 Q 50 10 65 35 Z" fill="#334155"/>
                    <circle cx="50" cy="28" r="4" fill="#38bdf8"/>
                    <polygon points="20,55 35,50 35,70" fill="#0f172a"/>
                    <polygon points="80,55 65,50 65,70" fill="#0f172a"/>
                    <polygon points="45,80 55,80 52,90 48,90" fill="#f59e0b"/>
                </svg>
            </div>
            <h2>כניסת מדריכים - צוות גיל</h2>
            <p>בחר מדריך או הזן אימייל וסיסמה:</p>

            <div class="quick-trainers-wrapper">
                <div class="quick-trainers-title">👥 כניסה מהירה לפי שם:</div>
                <div class="quick-trainers-chips">
                    <button type="button" class="trainer-chip-btn" onclick="selectQuickTrainer('itayhaker19@gmail.com')">איתי</button>
                    <button type="button" class="trainer-chip-btn" onclick="selectQuickTrainer('adielkassa@gmail.com')">עדיאל</button>
                    <button type="button" class="trainer-chip-btn" onclick="selectQuickTrainer('reemkayzer@gmail.com')">ראם</button>
                    <button type="button" class="trainer-chip-btn" onclick="selectQuickTrainer('nadavyichye@gmail.com')">נדב</button>
                    <button type="button" class="trainer-chip-btn" onclick="selectQuickTrainer('idolevko2@gmail.com')">עידו</button>
                    <button type="button" class="trainer-chip-btn" onclick="selectQuickTrainer('tomerk2001@gmail.com')">תומר</button>
                    <button type="button" class="trainer-chip-btn" onclick="selectQuickTrainer('netashatzberg@gmail.com')">נטע</button>
                    <button type="button" class="trainer-chip-btn" onclick="selectQuickTrainer('antonicbc@gmail.com')">מרקו</button>
                </div>
            </div>

            <input type="email" id="auth-email" name="email" class="login-input" placeholder="כתובת אימייל" required autocomplete="username">
            <input type="password" id="auth-pass" name="password" class="login-input" placeholder="סיסמה" required autocomplete="current-password">
            <button type="submit" id="loginBtn" class="login-btn">התחבר למערכת 🔐</button>
            <div id="error-msg"></div>
        </form>
    </div>

    <!-- תוכן האתר המלא -->
    <div id="main-content">
        <header>
            <div class="header-top">
                <h1>
                    <div style="display:inline-flex; align-items:center; justify-content:center; width:38px; height:38px; background:#f37021; border-radius:8px; box-shadow:0 2px 6px rgba(0,0,0,0.3); vertical-align:middle; overflow:hidden;">
                        <svg width="28" height="28" viewBox="0 0 100 100" style="transform: rotate(-45deg);">
                            <rect x="35" y="20" width="30" height="60" rx="15" fill="#1e293b"/>
                            <path d="M 35 35 Q 50 10 65 35 Z" fill="#334155"/>
                            <circle cx="50" cy="28" r="4" fill="#38bdf8"/>
                            <polygon points="20,55 35,50 35,70" fill="#0f172a"/>
                            <polygon points="80,55 65,50 65,70" fill="#0f172a"/>
                            <polygon points="45,80 55,80 52,90 48,90" fill="#f59e0b"/>
                        </svg>
                    </div>
                    תפעול והדרכה - צוות גיל
                </h1>
                <div class="header-actions-left">
                    <button id="themeToggleBtn" class="theme-toggle-btn" onclick="toggleTheme()">🌙 מצב כהה</button>
                    <button class="logout-btn" onclick="logout()">התנתק 🚪</button>
                </div>
            </div>
            <div class="nav-tabs">
                <button class="tab-btn active" onclick="switchTab('schedule', event)">📅 סידור עבודה</button>
                <button class="tab-btn" onclick="switchTab('dashboard', event)">📈 דשבורד</button>
                <button class="tab-btn" onclick="switchTab('todo-tab', event)">📝 משימות To-Do</button>
                <button class="tab-btn" onclick="switchTab('gorilla-status', event)">📊 סטטוס גורילות</button>
                <button class="tab-btn" onclick="switchTab('pdf-slides', event)">🔧 תקלות</button>
                <button class="tab-btn" onclick="switchTab('training-program', event)">🎓 הסמכה</button>
                <button class="tab-btn" onclick="switchTab('forms', event)">📋 טפסים והעשרה</button>
            </div>
        </header>

        <!-- באנר תזכורת פנימי למדריך המחובר -->
        <div id="todoUserReminderBanner" class="todo-user-reminder-banner" onclick="switchTab('todo-tab', event)">
            <span id="todoUserReminderText"></span>
            <span style="background:rgba(255,255,255,0.25); padding:2px 8px; border-radius:12px; font-size:0.8em;">לצפייה 👈</span>
        </div>

        <main>
            <!-- לשונית סידור עבודה -->
            <section id="schedule" class="tab-content active">
                <div class="trainer-profile-bar" id="trainerProfileBar">
                    <div class="trainer-info-text" id="trainerInfoDisplay">👤 לא זוהית כמדריך. אנא הזן פרטים:</div>
                    <div class="trainer-inputs-group" id="trainerInputsArea"></div>
                </div>

                <div class="schedule-header-action">
                    <h2 style="margin: 0; font-size: 1.15em;">📅 אימוני גורילות גיל - סידור עבודה חודשי ושבועי</h2>
                    <div class="search-box">
                        <input type="text" id="scheduleSearch" oninput="debouncedFilterSchedule()" placeholder="🔍 חפש מדריך, מיקום או יחידה בגיליון...">
                    </div>
                    <div class="action-btns-group">
                        <button class="wa-group-btn" id="waShiftsBtn" onclick="exportWeeklyShiftsToCalendar()">
                            <svg viewBox="0 0 24 24" style="width:16px;height:16px;fill:white;flex-shrink:0;"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981zm11.387-5.464c-.074-.124-.272-.198-.57-.347-.297-.149-1.758-.868-2.031-.967-.272-.099-.47-.149-.669.149-.198.297-.768.967-.941 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.521.151-.172.2-.296.3-.495.099-.198.05-.372-.025-.521-.075-.148-.669-1.611-.916-2.206-.242-.579-.487-.501-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.263.489 1.694.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414z"/></svg>
                            שלח משמרות שבוע לוואטסאפ
                        </button>
                        <button class="wa-group-btn" id="waGroupBtn" onclick="sendGroupWhatsAppSummary()">
                            <span>📋</span> סיכום שבועי לקבוצה
                        </button>
                    </div>
                </div>

                <div class="week-tabs-bar" id="weekTabsBar"></div>

                <div class="spreadsheet-container">
                    <div class="sheet-box">
                        <div class="sheet-side-header">
                            <span>ניידת 1 צפון</span>
                            <div class="header-btns-group">
                                <button class="unit-add-btn" onclick="addExtraRow('north')" title="הוסף שורה נוספת לתאריך">➕ הוסף שורה</button>
                                <button class="unit-wa-btn" onclick="sendTomorrowReminder('north')">
                                    <svg viewBox="0 0 24 24"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981zm11.387-5.464c-.074-.124-.272-.198-.57-.347-.297-.149-1.758-.868-2.031-.967-.272-.099-.47-.149-.669.149-.198.297-.768.967-.941 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.521.151-.172.2-.296.3-.495.099-.198.05-.372-.025-.521-.075-.148-.669-1.611-.916-2.206-.242-.579-.487-.501-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.263.489 1.694.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414z"/></svg>
                                    שלח הודעה למתאמנים של מחר
                                </button>
                            </div>
                        </div>
                        <div class="table-container">
                            <table id="sheetNorthTable">
                                <thead>
                                    <tr>
                                        <th>תאריך</th>
                                        <th>מדריך</th>
                                        <th>כוח מתאמן</th>
                                        <th>מיקום</th>
                                        <th>ישלט/אחוד</th>
                                        <th>איש קשר</th>
                                        <th>מס מתאמנים</th>
                                        <th>גורילה</th>
                                        <th>שעות</th>
                                        <th>הערות</th>
                                        <th>ניידת</th>
                                    </tr>
                                </thead>
                                <tbody id="northTableBody"></tbody>
                            </table>
                        </div>
                    </div>

                    <div class="sheet-box">
                        <div class="sheet-side-header">
                            <span>ניידת 2 מרכז/דרום</span>
                            <div class="header-btns-group">
                                <button class="unit-add-btn" onclick="addExtraRow('south')" title="הוסף שורה נוספת לתאריך">➕ הוסף שורה</button>
                                <button class="unit-wa-btn" onclick="sendTomorrowReminder('south')">
                                    <svg viewBox="0 0 24 24"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981zm11.387-5.464c-.074-.124-.272-.198-.57-.347-.297-.149-1.758-.868-2.031-.967-.272-.099-.47-.149-.669.149-.198.297-.768.967-.941 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.521.151-.172.2-.296.3-.495.099-.198.05-.372-.025-.521-.075-.148-.669-1.611-.916-2.206-.242-.579-.487-.501-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.263.489 1.694.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414z"/></svg>
                                    שלח הודעה למתאמנים של מחר
                                </button>
                            </div>
                        </div>
                        <div class="table-container">
                            <table id="sheetSouthTable">
                                <thead>
                                    <tr>
                                        <th>תאריך</th>
                                        <th>מדריך</th>
                                        <th>כוח מתאמן</th>
                                        <th>מיקום</th>
                                        <th>ישלט/אחוד</th>
                                        <th>איש קשר</th>
                                        <th>מס מתאמנים</th>
                                        <th>גורילה</th>
                                        <th>שעות</th>
                                        <th>הערות</th>
                                        <th>ניידת</th>
                                    </tr>
                                </thead>
                                <tbody id="southTableBody"></tbody>
                            </table>
                        </div>
                    </div>
                </div>

                <div class="month-folders-bar" id="monthFoldersBar"></div>
            </section>

            <!-- לשונית דשבורד סטטיסטי -->
            <section id="dashboard" class="tab-content">
                <div class="dashboard-header">
                    <h2>📈 דשבורד סטטיסטי</h2>
                    <p>תמונת מצב חיה של פעילות החודש, זמינות המאמנים ותקלות פתוחות. מתעדכן אוטומטית בכל שינוי.</p>
                </div>

                <!-- 4 כרטיסי KPI עליונים -->
                <div class="dashboard-kpi-grid">
                    <div class="kpi-card">
                        <div class="kpi-value" id="kpiTotalGorillas" style="color: #64748b;">7</div>
                        <div class="kpi-title">סה"כ גורילות</div>
                    </div>
                    <div class="kpi-card">
                        <div class="kpi-value" id="kpiHealthyGorillas" style="color: #22c55e;">0</div>
                        <div class="kpi-title">✅ תקינות</div>
                    </div>
                    <div class="kpi-card">
                        <div class="kpi-value" id="kpiFaultyGorillas" style="color: #ef4444;">0</div>
                        <div class="kpi-title">⚠️ לא תקינות</div>
                    </div>
                    <div class="kpi-card">
                        <div class="kpi-value" style="display: flex; align-items: center; justify-content: center; gap: 6px;">
                            <span id="kpiMonthTrainingDays" style="color: #0284c7;">0</span>
                            <span style="color: #64748b; font-size: 0.8em;">/</span>
                            <span id="kpiMonthCanceledDays" style="color: #ef4444;">0</span>
                        </div>
                        <div class="kpi-title">📅 ימי אימון חודשי <span style="color: #ef4444; font-size: 0.9em;">(ימים שבוטלו)</span></div>
                    </div>
                </div>

                <!-- גריד מרכזי: נתוני פעילות חודשית + נתוני גורילות -->
                <div class="dashboard-main-grid">
                    <div class="dashboard-box">
                        <div class="dashboard-box-title">
                            <span>📊 נתוני גורילות (ימים מאז טיפול מול ימי אימון)</span>
                            <span id="chartMonthLabel" style="font-size:0.8em; color:#0284c7;"></span>
                        </div>
                        <div style="position: relative; height: 280px; width: 100%;">
                            <canvas id="gorillaBarChart"></canvas>
                        </div>
                    </div>

                    <div class="dashboard-box">
                        <div class="dashboard-box-title">
                            <span>📋 סיכום פעילות - <span id="statsMonthTitle"></span></span>
                        </div>
                        <div class="stats-items-list">
                            <div class="stat-item-row">
                                <span class="stat-item-label">👥 סה"כ מתאמנים:</span>
                                <span class="stat-item-value" id="dashTotalTrainees">0</span>
                            </div>
                            <div class="stat-item-row">
                                <span class="stat-item-label">⏱️ סה"כ שעות פעילות (הערכה):</span>
                                <span class="stat-item-value" id="dashTotalHours">0 שעות</span>
                            </div>
                            <div class="stat-item-row" style="flex-direction: column; align-items: flex-start; gap: 6px;">
                                <span class="stat-item-label">📍 מיקומי אימון בחודש:</span>
                                <div class="badges-wrap" id="dashLocationsList"></div>
                            </div>
                            <div class="stat-item-row" style="flex-direction: column; align-items: flex-start; gap: 6px;">
                                <span class="stat-item-label">🛡️ כוחות מתאמנים (יחידות):</span>
                                <div class="badges-wrap" id="dashUnitsList"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- ריכוז תקלות פתוחות -->
                <div class="faults-section">
                    <div class="dashboard-box-title" style="border-bottom-color: rgba(239, 68, 68, 0.2); color: #ef4444;">
                        <span>🔧 תקלות פתוחות כרגע</span>
                        <span id="faultsCountBadge" style="font-size: 0.8em; background: #ef4444; color: white; padding: 2px 8px; border-radius: 10px;">0 תקלות</span>
                    </div>
                    <div id="openFaultsContainer"></div>
                </div>

                <!-- סרגל חודשים בתחתית הדשבורד -->
                <div class="month-folders-bar" id="dashboardMonthTabs"></div>
            </section>

            <!-- לשונית משימות To-Do -->
            <section id="todo-tab" class="tab-content">
                <div class="todo-container">
                    <div class="todo-header-box">
                        <h2>🚗 גורילות גיל - משימות לביצוע</h2>
                        <div style="display: flex; align-items: center; gap: 8px;">
                            <span id="todoCountDisplay" style="font-size:0.85em; color:#94a3b8; font-weight: bold;">0 משימות</span>
                        </div>
                    </div>

                    <!-- כרטיס הוספת משימה חדשה -->
                    <form class="todo-add-card" onsubmit="handleCreateTodo(event)">
                        <div class="todo-inputs-row">
                            <input type="text" id="todoTitleInput" class="todo-input-title" placeholder="➕ הוסף משימה חדשה..." required>
                            <select id="todoAssigneeSelect" class="todo-select-assignee">
                                <option value="">👤 ללא שיוך</option>
                                <option value="איתי הקר">איתי הקר</option>
                                <option value="עדיאל קסה">עדיאל קסה</option>
                                <option value="ראם קייזר">ראם קייזר</option>
                                <option value="נדב יחיא">נדב יחיא</option>
                                <option value="עידו לבקוביץ">עידו לבקוביץ</option>
                                <option value="תומר כחלון">תומר כחלון</option>
                                <option value="נטע שצברג">נטע שצברג</option>
                                <option value="מרקו">מרקו</option>
                            </select>
                            <input type="date" id="todoDueDateInput" class="todo-input-date" title="תאריך יעד לביצוע">
                            <button type="submit" class="todo-add-btn">הוסף 📌</button>
                        </div>
                    </form>

                    <!-- רשימת משימות פעילות -->
                    <div class="todo-list-wrap" id="activeTodoList"></div>

                    <!-- רשימת משימות שהושלמו -->
                    <div id="completedTodoSection" style="display:none; margin-top:20px;">
                        <h4 style="margin: 0 0 10px 0; font-size:0.9em; color:#94a3b8; border-bottom:1px solid var(--border-color); padding-bottom:4px;">
                            ✔️ הושלמו (<span id="completedCountDisplay">0</span>)
                        </h4>
                        <div class="todo-list-wrap" id="completedTodoList"></div>
                    </div>
                </div>
            </section>

            <!-- לשונית סטטוס גורילות -->
            <section id="gorilla-status" class="tab-content">
                <h2>📊 סטטוס גורילות</h2>
                <p style="color: #64748b; margin-bottom: 15px; font-size: 0.85em;">מעקב ועדכון סטטוס תקינות למאמני הגורילה (שינוי סטטוס מעדכן הערות וצבעים).</p>
                <div class="status-table-container">
                    <table class="schedule-table">
                        <thead>
                            <tr>
                                <th>גורילה</th>
                                <th>תקין/תקול</th>
                                <th>טיפול חודשי אחרון</th>
                                <th>תקלה/הערות נוספות</th>
                            </tr>
                        </thead>
                        <tbody id="statusTableBody">
                            <tr data-id="0"><td class="gorilla-name-cell" style="font-weight: bold; background: #27ae60; color: white;">גורילה מס 1</td><td><select class="status-select" onchange="updateRowStatus(this)"><option value="תקין" selected>תקין</option><option value="לא תקין">לא תקין</option></select></td><td><div class="cleaning-date-wrapper"><button type="button" class="cleaning-today-btn" onclick="openCleaningPicker(this)">27/07</button><input type="date" class="cleaning-date-input" onchange="onCleaningDateChange(this)" style="position:absolute; opacity:0; pointer-events:none; width:1px; height:1px;"></div></td><td><input type="text" class="notes-input" value="יש מפות חדשות+ הותקן רפאלו מחדש" oninput="saveStatusData()"></td></tr>
                            <tr data-id="1"><td class="gorilla-name-cell" style="font-weight: bold; background: #e74c3c; color: white;">גורילה מס 2</td><td><select class="status-select" onchange="updateRowStatus(this)"><option value="תקין">תקין</option><option value="לא תקין" selected>לא תקין</option></select></td><td><div class="cleaning-date-wrapper"><button type="button" class="cleaning-today-btn" onclick="openCleaningPicker(this)">27/07</button><input type="date" class="cleaning-date-input" onchange="onCleaningDateChange(this)" style="position:absolute; opacity:0; pointer-events:none; width:1px; height:1px;"></div></td><td><input type="text" class="notes-input" value="לא ידוע." oninput="saveStatusData()"></td></tr>
                            <tr data-id="2"><td class="gorilla-name-cell" style="font-weight: bold; background: #27ae60; color: white;">גורילה מס 3</td><td><select class="status-select" onchange="updateRowStatus(this)"><option value="תקין" selected>תקין</option><option value="לא תקין">לא תקין</option></select></td><td><div class="cleaning-date-wrapper"><button type="button" class="cleaning-today-btn" onclick="openCleaningPicker(this)">27/07</button><input type="date" class="cleaning-date-input" onchange="onCleaningDateChange(this)" style="position:absolute; opacity:0; pointer-events:none; width:1px; height:1px;"></div></td><td><input type="text" class="notes-input" value="קופסאת ממשקים תקולה (VGA) צריך לבדוק עם מתאם חדש" oninput="saveStatusData()"></td></tr>
                            <tr data-id="3"><td class="gorilla-name-cell" style="font-weight: bold; background: #e74c3c; color: white;">גורילה מס 4</td><td><select class="status-select" onchange="updateRowStatus(this)"><option value="תקין">תקין</option><option value="לא תקין" selected>לא תקין</option></select></td><td><div class="cleaning-date-wrapper"><button type="button" class="cleaning-today-btn" onclick="openCleaningPicker(this)">27/07</button><input type="date" class="cleaning-date-input" onchange="onCleaningDateChange(this)" style="position:absolute; opacity:0; pointer-events:none; width:1px; height:1px;"></div></td><td><input type="text" class="notes-input" value="טכנאי צריך להלבין, קיבל הצפנה משלום +עדכון מפות" oninput="saveStatusData()"></td></tr>
                            <tr data-id="4"><td class="gorilla-name-cell" style="font-weight: bold; background: #27ae60; color: white;">גורילה מס 5</td><td><select class="status-select" onchange="updateRowStatus(this)"><option value="תקין" selected>תקין</option><option value="לא תקין">לא תקין</option></select></td><td><div class="cleaning-date-wrapper"><button type="button" class="cleaning-today-btn" onclick="openCleaningPicker(this)">27/07</button><input type="date" class="cleaning-date-input" onchange="onCleaningDateChange(this)" style="position:absolute; opacity:0; pointer-events:none; width:1px; height:1px;"></div></td><td><input type="text" class="notes-input" value="יש מפות חדשות+ הותקן רפאלו מחדש" oninput="saveStatusData()"></td></tr>
                            <tr data-id="5"><td class="gorilla-name-cell" style="font-weight: bold; background: #27ae60; color: white;">גורילה מס 6</td><td><select class="status-select" onchange="updateRowStatus(this)"><option value="תקין" selected>תקין</option><option value="לא תקין">לא תקין</option></select></td><td><div class="cleaning-date-wrapper"><button type="button" class="cleaning-today-btn" onclick="openCleaningPicker(this)">27/07</button><input type="date" class="cleaning-date-input" onchange="onCleaningDateChange(this)" style="position:absolute; opacity:0; pointer-events:none; width:1px; height:1px;"></div></td><td><input type="text" class="notes-input" value="יש מפות חדשות+ הותקן רפאלו מחדש" oninput="saveStatusData()"></td></tr>
                            <tr data-id="6"><td class="gorilla-name-cell" style="font-weight: bold; background: #e74c3c; color: white;">גורילה מס 7</td><td><select class="status-select" onchange="updateRowStatus(this)"><option value="תקין">תקין</option><option value="לא תקין" selected>לא תקין</option></select></td><td><div class="cleaning-date-wrapper"><button type="button" class="cleaning-today-btn" onclick="openCleaningPicker(this)">27/07</button><input type="date" class="cleaning-date-input" onchange="onCleaningDateChange(this)" style="position:absolute; opacity:0; pointer-events:none; width:1px; height:1px;"></div></td><td><input type="text" class="notes-input" value="יש מפות חדשות+ הותקן רפאלו מחדש" oninput="saveStatusData()"></td></tr>
                        </tbody>
                    </table>
                </div>
            </section>

            <!-- לשונית תקלות -->
            <section id="pdf-slides" class="tab-content">
                <h2>🔧 מדריך תפעול ופתרון תקלות - גורילה גיל</h2>
                <p style="color: #64748b; margin-bottom: 12px; font-size: 0.85em;">סדר פעולות מפורט לפתרון תקלות נפוצות במאמן גורילה גיל לפי שלבי עבודה.</p>

                <div style="display: flex; gap: 10px; margin-bottom: 15px; flex-wrap: wrap;">
                    <a href="tel:0526652209" class="call-btn" style="flex: 1; min-width: 200px; justify-content: center; padding: 12px; font-size: 0.9em;">
                        <span>📞</span> צלצל לקסה
                    </a>
                    <a href="tel:0526620187" class="call-btn" style="flex: 1; min-width: 200px; justify-content: center; padding: 12px; font-size: 0.9em;">
                        <span>📞</span> צלצל לטכנאי
                    </a>
                </div>

                <div class="search-box" style="margin-bottom: 15px;">
                    <input type="text" id="slidesSearch" oninput="debouncedFilterSlides()" placeholder="🔍 חפש תקלה או מילת מפתח (למשל: משגר, קומים, תלת מימד, טיל תקול)...">
                </div>

                <div id="slidesContainer">
                    <div class="slide-box">
                        <h3 class="slide-title">🔌 הדלקת הגורילה - סדר פעולות תקני</h3>
                        <ol class="step-list">
                            <li><strong>חיבור כבל קומקום לגורילה</strong> (כששום דבר אחר לא מחובר). הדלקת המתג + המתנה של 2 שניות.</li>
                            <li><strong>הדלקת מחשב ראשי</strong> – לחיצה של 2 שניות.</li>
                            <li><strong>לחיצה על הכפתור הקטן</strong>.</li>
                            <li><strong>חיבור שאר קופסת הממשקים</strong> בזמן שהתרגיל נטען במערכת.</li>
                        </ol>
                        <div class="slide-img-box">
                            <img src="https://pvtswscsqnymbbzgsafu.supabase.co/storage/v1/object/public/media/2.jpg.png" alt="הדלקת הגורילה" loading="lazy">
                        </div>
                    </div>

                    <div class="slide-box">
                        <h3 class="slide-title">🚀 תקלות משגר, חיבורי SPARTACUS ופתרון ריצוד</h3>
                        <div class="step-list">
                            <div class="slide-img-box">
                                <img src="https://pvtswscsqnymbbzgsafu.supabase.co/storage/v1/object/public/media/1.jpg.png" alt="תקלות משגר וחיבורי SPARTACUS" loading="lazy">
                            </div>

                            <p><strong>1. לא מזהה משגר / אין תנועה במשגר:</strong></p>
                            <ul>
                                <li>פותחים את אפליקציית <strong>SPARTACUS</strong> ובודקים אם <span class="code-block">COM3</span> מתחבר.</li>
                                <li>אם <span class="code-block">COM3</span> לא מתחבר, לוחצים על <strong>Device Settings</strong>.</li>
                                <li>בודקים איזה קום מחובר כעת ברשימה (1, 3, 4, 5).</li>
                                <li>לוחצים על <strong>Advance</strong> וממתינים עד להופעת תמונת המטוס/מד האופק.</li>
                                <li>אם עדיין לא מתחבר - עוברים מיידית לסידור קומים ב-Windows.</li>
                            </ul>
                            <p><strong>2. סידור קומים (Device Manager):</strong></p>
                            <div class="slide-img-box">
                                <img src="https://pvtswscsqnymbbzgsafu.supabase.co/storage/v1/object/public/media/6.jpg.png" alt="סידור קומים ב-Device Manager" loading="lazy">
                            </div>
                            <ul>
                                <li>מקלידים בשורת החיפוש ב-Windows: <strong>Device Manager</strong> (מנהל ההתקנים).</li>
                                <li>נכנסים לתיקיית <strong>PORTS (COM & LPT)</strong> – יש לוודא הופעת 4 קומים:
                                    <ul>
                                        <li><strong>COM1:</strong> היציאה הארוכה (Prolific PL2303GC USB Serial COM Port)</li>
                                        <li><strong>COM3:</strong> USB Serial Port</li>
                                        <li><strong>COM4:</strong> USB Serial Port</li>
                                        <li><strong>COM5:</strong> USB-SERIAL CH340</li>
                                    </ul>
                                </li>
                                <li><strong style="color:#e74c3c;">דגש קריטי:</strong> אסור בשום אופן להגדיר את אותו מספר קום פעמיים!</li>
                            </ul>
                            <div class="slide-video-container">
                                <h4>🎬 סרטון הדרכה: סידור קומים גורילת גיל</h4>
                                <div class="video-wrapper">
                                    <iframe src="https://www.youtube.com/embed/yct6JCOWgIs" title="סידור קומים גורילת גיל" loading="lazy" allowfullscreen></iframe>
                                </div>
                                <a href="https://youtu.be/yct6JCOWgIs" target="_blank" class="yt-link-btn">▶️ צפה ב-YouTube</a>
                            </div>
                        </div>
                    </div>

                    <div class="slide-box">
                        <h3 class="slide-title">🖥️ תקלות תצוגה ומסכים</h3>
                        <div class="step-list">
                            <div class="slide-img-box">
                                <img src="https://pvtswscsqnymbbzgsafu.supabase.co/storage/v1/object/public/media/5.jpg.png" alt="תקלות תצוגה ומסכים" loading="lazy">
                            </div>

                            <p><strong>1. מסך שחור בישלט (כאשר ב-IOS רואים תמונה תקינה):</strong></p>
                            <ul>
                                <li>מנתקים את כבל <strong>9P</strong> מגב היחידה ומחברים אותו מחדש בחוזקה.</li>
                            </ul>
                            <p><strong>2. סידור מסכים ב-Display Settings והגדרת HZ60.32:</strong></p>
                            <div class="slide-img-box">
                                <img src="https://pvtswscsqnymbbzgsafu.supabase.co/storage/v1/object/public/media/7.jpg.png" alt="סידור מסכים - הגדרת הרץ" style="margin-bottom: 8px;" loading="lazy">
                                <img src="https://pvtswscsqnymbbzgsafu.supabase.co/storage/v1/object/public/media/8.jpg.png" alt="סידור מסכים - רזולוציות" loading="lazy">
                            </div>
                            <ul>
                                <li>נכנסים ל-Display Settings בווינדוס -> לוחצים על <strong>Advanced display</strong>.</li>
                                <li>מוודאים שקצב הרענון מוגדר בדיוק על <span class="code-block">60.32 Hz</span>.</li>
                                <li>סידור מסכים: <strong>מספרי המסכים לא רלוונטיים</strong> – העיקר שיהיו <strong>3 מסכים גדולים ו-1 קטן</strong>.</li>
                                <li>רזולוציות: המסכים הגדולים <span class="code-block">1080X1920</span> והמסך הקטן <span class="code-block">600X800</span>.</li>
                            </ul>
                            <div class="slide-video-container">
                                <h4>🎬 סרטון הדרכה: פתרון תקלה כאשר תלת מימד לא עולה</h4>
                                <div class="video-wrapper">
                                    <iframe src="https://www.youtube.com/embed/_SPomcHd1VU" title="תלת מימד לא עולה" loading="lazy" allowfullscreen></iframe>
                                </div>
                                <a href="https://youtu.be/_SPomcHd1VU" target="_blank" class="yt-link-btn">▶️ צפה ב-YouTube</a>
                            </div>
                        </div>
                    </div>

                    <div class="slide-box">
                        <h3 class="slide-title">💥 תקלות קריסת מערכת ופריקת מתח</h3>
                        <div class="step-list">
                            <p><strong>1. פריקת מתח מלאה בגורילה:</strong></p>
                            <ul>
                                <li>כיבוי מלא של המערכת באמצעות הכפתור האדום. הוצאת כבל הקומקום, לחיצות מהירות על כפתור ההפעלה עד הבהוב במסכים.</li>
                            </ul>
                            <div class="slide-video-container">
                                <h4>🎬 סרטון הדרכה: פריקת מתח גורילה</h4>
                                <div class="video-wrapper">
                                    <iframe src="https://www.youtube.com/embed/gfm4laG0SYo" title="פריקת מתח גורילה" loading="lazy" allowfullscreen></iframe>
                                </div>
                                <a href="https://youtube.com/shorts/gfm4laG0SYo" target="_blank" class="yt-link-btn">▶️ צפה ב-YouTube</a>
                            </div>
                            <p><strong>2. פרוססים לא עולים / תהליך תקוע:</strong></p>
                            <ul>
                                <li>מנהל המשימות -> Services -> איתור <strong>AppsControlManager</strong> -> קליק ימני Stop -> ואז Start.</li>
                            </ul>
                        </div>
                    </div>

                    <div class="slide-box">
                        <h3 class="slide-title">📁 העברת תרגילים בין גורילות (מולבנת למולבנת)</h3>
                        <div class="slide-img-box">
                            <img src="https://pvtswscsqnymbbzgsafu.supabase.co/storage/v1/object/public/media/4.jpg.png" alt="העברת תרגילים בין גורילות" loading="lazy">
                        </div>
                        <ol class="step-list">
                            <li>חיבור כבל תקשורת רשת ישיר בין הגורילות.</li>
                            <li><strong>שינוי IP בווינדוס:</strong> הזינו <span class="code-block">NCP</span> בווינדוס -> שינוי IP בלאונצ'ר ל- <span class="code-block">10.0.0.8</span> למקור ו ל- <span class="code-block">10.0.0.96</span> ליעד.</li>
                            <li>הזינו נתיב <span class="code-block">\\10.0.0.8\c</span> ובחרו בתרחישים הרצויים.</li>
                        </ol>
                        <div class="videos-flex-container">
                            <div class="slide-video-container">
                                <h4>🎬 סרטון הדרכה: העברת תרגילים בין גורילות</h4>
                                <div class="video-wrapper">
                                    <iframe src="https://www.youtube.com/embed/D4wlKqKUk1o" title="העברת תרגילים בין גורילות" loading="lazy" allowfullscreen></iframe>
                                </div>
                                <a href="https://youtube.com/shorts/D4wlKqKUk1o" target="_blank" class="yt-link-btn">▶️ צפה ב-YouTube</a>
                            </div>
                            <div class="slide-video-container">
                                <h4>🎬 סרטון הדרכה: חיבור הגדרות רשת ותקשורת</h4>
                                <div class="video-wrapper">
                                    <iframe src="https://www.youtube.com/embed/W6bQJojtayQ" title="רשתות" loading="lazy" allowfullscreen></iframe>
                                </div>
                                <a href="https://youtu.be/W6bQJojtayQ" target="_blank" class="yt-link-btn">▶️ צפה ב-YouTube</a>
                            </div>
                        </div>
                    </div>

                    <div class="slide-box">
                        <h3 class="slide-title">📥 התקנת / עדכון דרייברים של NVIDIA</h3>
                        <div class="slide-img-box">
                            <img src="https://pvtswscsqnymbbzgsafu.supabase.co/storage/v1/object/public/media/3.jpg.png" alt="התקנת דרייברים של NVIDIA" loading="lazy">
                        </div>
                        <div class="step-list">
                            <ol>
                                <li><strong style="color: #ef4444;">חובה:</strong> לנתק את 4 הכבלים (משמאל לימין) לפני הדלקת המערכת!</li>
                                <li>פתיחת סייר הקבצים (<span class="code-block">Win + E</span>) -> מעבר לנתיב: <span class="code-block">C:\IT\NEW VERSION May 2025</span>.</li>
                                <li>הרצת קובץ ההתקנה -> לחיצה על <strong>Nvidia Graphics Driver</strong> -> לחיצה על <strong>AGREE AND CONTINUE</strong>.</li>
                                <li>בחלון Installation options: בחירה ב-<strong>Express (Recommended)</strong> -> לחיצה על <strong>NEXT</strong>.</li>
                                <li>בסיום ההתקנה – ביצוע הפעלה מחדש (Restart) למחשב.</li>
                            </ol>
                        </div>
                    </div>

                    <div class="slide-box" style="border-right-color: #ef4444;">
                        <h3 class="slide-title">🎯 טיפול בתקלות טיל תקול ובעיות באחוד מבצעי</h3>
                        <div class="step-list">
                            <ul>
                                <li><strong style="color: #ef4444;">כל תקלה של טיל תקול החלף, שו״ש בלבד</strong></li>
                                <li><strong>פתרון:</strong> כיבוי הדלקה ואם לא עובד אז ביט למשגר</li>
                            </ul>
                        </div>
                    </div>

                    <div class="slide-box">
                        <h3 class="slide-title">🧹 ניקיון ותחזוקה חודשית לגורילה</h3>
                        <ol class="step-list">
                            <li><strong>ניקיון כללי:</strong> ניקוי בלחץ אוויר וניגוב במטלית לחה.</li>
                            <li><strong>אחזקה פיזית:</strong> בדיקת תקינות גלגלים ופרפריות הידוק.</li>
                            <li><strong>צמות וחיבורים:</strong> בדיקת שלמות צמות הכבלים והמחברים לגורילה.</li>
                            <li><strong>בדיקת אש:</strong> ביצוע שיגור טיל בדיקה.</li>
                            <li><strong>תחזוקת רכבים:</strong> פינוי אשפה, שאיבה, ניגוב במגבונים ושטיפה בשטיפומט.</li>
                            <li><strong>פירוק רשת ופילטרים:</strong> הוצאת 10 ברגים (5 מכל צד), הרמת הרשת וניקוי עם מפוח אוויר ממרחק בטוח!</li>
                        </ol>
                    </div>
                </div>
            </section>

            <!-- לשונית הסמכה -->
            <section id="training-program" class="tab-content">
                <h2>🎓 תוכנית הסמכה - מנהל אתר גיל נייד</h2>
                <p style="font-size: 0.85em; margin-bottom: 15px;"><strong>מפתח הסמכה מבוקר:</strong> ILS014D | <strong>תחולה:</strong> 02/2014</p>

                <h3 class="table-title">יום מס' 1 - כללי: הכרת החברה ואופן העבודה</h3>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr><th>נושא נלמד</th><th>חופף</th><th>תוכן והנחיות</th><th>קישור ישיר</th></tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>הכרת החברה</td><td>מנהל אתר</td>
                                <td>פריסת המאמנים בארץ ובעולם, תחומי העיסוק של החברה, מחלקת התפעול וצוות החיי''ר, הצהרת האיכות.</td>
                                <td><a href="https://msbagiraadmoutlook.sharepoint.com/:p:/r/Operations/Infantry_Department/_layouts/15/Doc.aspx?sourcedoc=%7B71638794-805A-4E40-A191-53AE2320BE46%7D&action=edit" target="_blank" class="link-table-btn">📂 מצגת חברה</a></td>
                            </tr>
                            <tr>
                                <td>הצגת מוצרים</td><td>מנהל אתר</td>
                                <td>הצגת מוצרי החברה.</td>
                                <td><a href="https://msbagiraadmoutlook.sharepoint.com/:p:/r/Operations/Infantry_Department/_layouts/15/Doc.aspx?sourcedoc=%7B71638794-805A-4E40-A191-53AE2320BE46%7D&action=edit" target="_blank" class="link-table-btn">📂 מצגת מוצרים</a></td>
                            </tr>
                            <tr>
                                <td>אופן העבודה במחלקת התפעול</td><td>מנהל אתר</td>
                                <td>מבנה ארגוני ובעלי תפקידים, ממשקים - רכזת תפעול, מנהל צוות חיי''ר, מנהלי אזורים.</td>
                                <td><a href="https://msbagiraadmoutlook.sharepoint.com/:p:/r/Operations/Infantry_Department/_layouts/15/Doc.aspx?sourcedoc=%7B71638794-805A-4E40-A191-53AE2320BE46%7D&action=edit" target="_blank" class="link-table-btn">📂 מצגת מבנה</a></td>
                            </tr>
                            <tr>
                                <td>טיל הגיל בצה''ל</td><td>מנהל אתר</td>
                                <td>למידה על שימוש טיל הגיל בצה''ל בעבר וכיום, סוגי משגרים, סוגי טילים.</td>
                                <td>-</td>
                            </tr>
                            <tr>
                                <td>ירי תחושה</td><td>מנהל אתר</td>
                                <td>הכרת אמצעי חשיפה תקיפה המצויים כיום בצה''ל - הכולל משגרים + אמצעי תצפית.</td>
                                <td>-</td>
                            </tr>
                        </tbody>
                    </table>
                </div>

                <h3 class="table-title">יום מס' 2 - תפעול: שיעורי תפעול והעלאת מערכות</h3>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr><th>נושא נלמד</th><th>חופף</th><th>תוכן והנחיות</th><th>קישור ישיר</th></tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>שיעור העלאת מערכות</td><td>מנהל אתר</td>
                                <td>הדלקת המערכת תוך הסבר על המרכיבים השונים, הפעלת אימון כוון בודד, כיבוי מערכות.</td>
                                <td><a href="https://msbagiraadmoutlook.sharepoint.com/:p:/r/Operations/Infantry_Department/_layouts/15/Doc.aspx?sourcedoc=%7B7F33D2D0-628A-4D16-9B34-35F87E0F66FD%7D&action=edit" target="_blank" class="link-table-btn">📂 מצגת העלאה</a></td>
                            </tr>
                            <tr>
                                <td>שיעור החלפת אמצעים</td><td>מנהל אתר</td>
                                <td>החלפת אמצעים מאחוד לישלט וההפך (כולל ספרטון - אינקודר).</td>
                                <td>-</td>
                            </tr>
                            <tr>
                                <td>כיבוי מערכות</td><td>מנהל אתר</td>
                                <td>כיבוי מערכות לפי הסדר והחזרת המאמן למצב אפס (סידור של המאמן לאימון למחרת).</td>
                                <td>-</td>
                            </tr>
                        </tbody>
                    </table>
                </div>

                <h3 class="table-title">יום מס' 3+4 - אימון כוון בודד: תרגול הרמת מערכות וניהול אימון</h3>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr><th>נושא נלמד</th><th>חופף</th><th>תוכן והנחיות</th><th>קישור ישיר</th></tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>תרגול הרמת מערכות ותפעול</td><td>מנהל אתר</td>
                                <td>תרגול של החניך עם סיוע מנהל האתר, מהות ואופן ביצוע תתרגול תפעול.</td>
                                <td>-</td>
                            </tr>
                            <tr>
                                <td>מצגת תקלות ותפעול</td><td>מנהל אתר</td>
                                <td>תפעול תקלות נפוצות במערכת.</td>
                                <td><a href="https://msbagiraadmoutlook.sharepoint.com/:p:/r/Operations/Infantry_Department/_layouts/15/Doc.aspx?sourcedoc=%7B6AC2CED7-975E-4845-9310-1B5F76503B21%7D&action=edit" target="_blank" class="link-table-btn">📂 מצגת תקלות</a></td>
                            </tr>
                            <tr>
                                <td>תרגול ניהול אימון וסיכום</td><td>מנהל אתר</td>
                                <td>העברת אימון לחניך כוון בודד, סיכום עם המתאמנים, משוב וסגירת מערכות.</td>
                                <td>-</td>
                            </tr>
                        </tbody>
                    </table>
                </div>

                <h3 class="table-title">יום מס' 5 - חניכת אימון ומבחנים: תרגול, תקלות ומבחן עיוני</h3>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr><th>נושא נלמד</th><th>חופף</th><th>תוכן והנחיות</th><th>קישור ישיר</th></tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>תרגול הרמת מערכות ותקלות</td><td>מנהל אתר</td>
                                <td>תרגול מעשי של החניך בליווי מנהל האתר, מעבר על מצגת תקלות.</td>
                                <td>-</td>
                            </tr>
                            <tr>
                                <td>מבחן עיוני</td><td>מנהל אתר</td>
                                <td>ביצוע מבחן עיוני כתוב.</td>
                                <td><a href="https://msbagiraadmoutlook.sharepoint.com/:w:/g/Operations/Infantry_Department/IQCucOPovSqGT7PZLCqrMj93AZdmLZ17258Uo9X2NqYvnE0?e=Wwm1lj" target="_blank" class="link-table-btn" style="background-color: #2ecc71;">✍️ פתח מבחן עיוני 🔗</a></td>
                            </tr>
                        </tbody>
                    </table>
                </div>

                <h3 class="table-title">יום מס' 6 - ניהול אתר ומבחן מעשי: ניהול אתר מלא, נהלים ומבחן מעשי</h3>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr><th>נושא נלמד</th><th>חופף</th><th>תוכן והנחיות</th><th>קישור ישיר</th></tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>הפעלת אימון וניהול אתר</td><td>מנהל אתר</td>
                                <td>יישום עצמאי של יום אימון מלא בחניכת מנהל אתר, הכרת נהלי דיווח, אחזקה וובלט.</td>
                                <td><a href="https://msbagiraadmoutlook.sharepoint.com/:w:/r/Quality_Assurance/_layouts/15/Doc.aspx?sourcedoc=%7BB11E7533-0094-430C-9374-4767C76DB949%7D&action=default" target="_blank" class="link-table-btn">📄 נוהל דיווחים</a></td>
                            </tr>
                            <tr>
                                <td>מבחן מעשי וסיכום חפיפה</td><td>מנהל צוות/מחלקה</td>
                                <td>ביצוע מבחן מעשי, מעבר על תכנית ההסמכה וסיכום חפיפה.</td>
                                <td>-</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </section>

            <!-- לשונית טפסים והעשרה -->
            <section id="forms" class="tab-content">
                <h2>📋 טפסים, ציוד והעשרה</h2>
                
                <div class="search-box" style="margin-bottom: 15px;">
                    <input type="text" id="formsSearch" oninput="debouncedFilterForms()" placeholder="🔍 חפש טופס, רכב, נתוני גיל, מרעום, זום, טווח...">
                </div>

                <div class="cards-container">
                    <div class="card form-item">
                        <div class="form-card-content">
                            <div class="form-info">
                                <h3>🚗 רשימת ציוד לרכב</h3>
                                <p style="font-size: 0.85em; margin-bottom: 8px;">טופס לבדיקה ומילוי דיווח ציוד רכב.</p>
                                <a href="https://forms.cloud.microsoft/r/YQWDPAaeUe" target="_blank" class="btn">לפתיחת הטופס 🔗</a>
                            </div>
                            <div class="form-qr-box">
                                <img src="https://api.qrserver.com/v1/create-qr-code/?size=120x120&data=https://forms.cloud.microsoft/r/YQWDPAaeUe" alt="QR Code" loading="lazy">
                                <span class="form-url-text">forms.cloud.microsoft/r/YQWDPAaeUe</span>
                                <button class="copy-btn" onclick="copyText('https://forms.cloud.microsoft/r/YQWDPAaeUe', this)">📋 העתק</button>
                            </div>
                        </div>
                    </div>

                    <div class="card form-item">
                        <div class="form-card-content">
                            <div class="form-info">
                                <h3>✍️ משוב מתאמנים</h3>
                                <p style="font-size: 0.85em; margin-bottom: 8px;">טופס איסוף רשמים ומשוב מהמתאמנים.</p>
                                <a href="https://forms.cloud.microsoft/r/u1afBRvv3q" target="_blank" class="btn">לפתיחת הטופס 🔗</a>
                            </div>
                            <div class="form-qr-box">
                                <img src="https://api.qrserver.com/v1/create-qr-code/?size=120x120&data=https://forms.cloud.microsoft/r/u1afBRvv3q" alt="QR Code" loading="lazy">
                                <span class="form-url-text">forms.cloud.microsoft/r/u1afBRvv3q</span>
                                <button class="copy-btn" onclick="copyText('https://forms.cloud.microsoft/r/u1afBRvv3q', this)">📋 העתק</button>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="card form-item" style="width: 100%; margin-top: 15px;">
                    <h3 style="margin-top: 0; color: var(--text-color); border-bottom: 2px solid var(--border-color); padding-bottom: 8px;">🚀 העשרה - נתוני טיל גיל</h3>
                    <p style="font-size: 0.85em; color: #64748b; margin-bottom: 12px;">ריכוז נתונים טכניים, זמני מעוף, מצבי מרעום ומעטפת בטיחות:</p>
                    
                    <h4 style="margin: 12px 0 6px 0; font-size: 0.95em; color: var(--link-color);">🔍 השוואת דגמים (גיל 1 מול גיל 2)</h4>
                    <div class="table-container" style="margin-bottom: 15px;">
                        <table style="width: 100%; text-align: center; border-collapse: collapse; font-size: 0.82em;">
                            <thead>
                                <tr style="background-color: var(--th-bg); color: white;">
                                    <th style="padding: 8px;">פרמטר</th>
                                    <th style="padding: 8px;">גיל 1</th>
                                    <th style="padding: 8px;">גיל 2</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">זום / הגדלה</td>
                                    <td style="padding: 8px;">10X / 30X</td>
                                    <td style="padding: 8px;">5X / 10X / 20X</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">רדיוס הרג ופציעה</td>
                                    <td style="padding: 8px;">הרג 8 מטרים | פציעה 15 מטרים</td>
                                    <td style="padding: 8px;">הרג 2.5–3 מטרים | פציעה 15 מטרים</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">זמן מעוף לטווח מקסימלי</td>
                                    <td style="padding: 8px;"><span class="code-block">26 שניות</span></td>
                                    <td style="padding: 8px;"><span class="code-block">53 שניות</span></td>
                                </tr>
                            </tbody>
                        </table>
                    </div>

                    <h4 style="margin: 12px 0 6px 0; font-size: 0.95em; color: var(--link-color);">🎯 מצבי מרעום / סוגי מטרות</h4>
                    <div class="table-container" style="margin-bottom: 15px;">
                        <table style="width: 100%; text-align: center; border-collapse: collapse; font-size: 0.82em;">
                            <thead>
                                <tr style="background-color: var(--th-bg); color: white;">
                                    <th style="padding: 8px;">סוג מטרה</th>
                                    <th style="padding: 8px;">מנגנון יזום ואופן הפעולה</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">קשה</td>
                                    <td style="padding: 8px;">חודר</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">רכה</td>
                                    <td style="padding: 8px;">מתפוצץ 30 ס"מ לפני המטרה</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">רסס</td>
                                    <td style="padding: 8px;">מרעום קרבה – 70 ס"מ לפני המטרה</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>

                    <h4 style="margin: 12px 0 6px 0; font-size: 0.95em; color: var(--link-color);">☁️ ירי בעננות, ניהוג וסחיפת נעילה</h4>
                    <div class="table-container" style="margin-bottom: 15px;">
                        <table style="width: 100%; text-align: center; border-collapse: collapse; font-size: 0.82em;">
                            <thead>
                                <tr style="background-color: var(--th-bg); color: white;">
                                    <th style="padding: 8px; width: 30%;">תרחיש / מצב</th>
                                    <th style="padding: 8px;">אופן פעולה והנחיות</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">עננות נמוכה</td>
                                    <td style="padding: 8px;">נשגר במעוף נמוך.</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">מטרת NLOS (ללא אפשרות למעוף נמוך)</td>
                                    <td style="padding: 8px;">נשגר בניהוג.</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">כניסה לעננות במצב נעילה</td>
                                    <td style="padding: 8px;">עלולה להתרחש סחיפת נעילה שעלולה להוביל לניהוג זמני.</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">ניהוג זמני בגיל 1</td>
                                    <td style="padding: 8px;">סחיפת נעילה ועדכון רציף של הכוון תכניס אותנו למצב זה.</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">ניהוג זמני בגיל 2</td>
                                    <td style="padding: 8px;">המערכת יודעת להתגבר לבד על סחיפת נעילה, ובגלל זה <strong>אין מצב מוגדר של ניהוג זמני</strong>.</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold; color: #ef4444;">חריגה ממשפך בטיחות</td>
                                    <td style="padding: 8px;">במידה והטיל נסחף ועובר את משפך הבטיחות (<span class="code-block">2500 לצדדים</span>) – הטיל יפיל את עצמו.</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>

                    <h4 style="margin: 12px 0 6px 0; font-size: 0.95em; color: var(--link-color);">⚙️ מעטפת שיגור, בטיחות ומעוף</h4>
                    <div class="table-container">
                        <table style="width: 100%; text-align: center; border-collapse: collapse; font-size: 0.82em;">
                            <thead>
                                <tr style="background-color: var(--th-bg); color: white;">
                                    <th style="padding: 8px;">נושא / פרמטר</th>
                                    <th style="padding: 8px;">נתון / פירוט</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">מהירות הטיל</td>
                                    <td style="padding: 8px;"><span class="code-block">150 מטר/שנייה</span></td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">טווח ירי מינימלי</td>
                                    <td style="padding: 8px;">450 מטרים</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">מגבלת מזג אוויר</td>
                                    <td style="padding: 8px; color: #ef4444; font-weight: bold;">איסור שיגור ברוח מעל 50 קמ"ש</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">תנאי יזום (מ-150 מטר)</td>
                                    <td style="padding: 8px;">
                                        טיל יכול ליזום לאחר 150 מטר בהתקיים 3 תנאים:
                                        <br>
                                        1. פתיחת כנפיים &nbsp;|&nbsp; 2. מעבר 150 מטר &nbsp;|&nbsp; 3. כוח עומס של 7G
                                    </td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">TIPP OFF (יציאה מהזביל)</td>
                                    <td style="padding: 8px;">נפילה של 60 ס"מ ב-8 המטרים הראשונים</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">הצתת מנוע ראשי</td>
                                    <td style="padding: 8px;">ניצת רק לאחר 3.5 מטרים (להגנת המפעיל)</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">רשף לאחור</td>
                                    <td style="padding: 8px;">2.7 מטרים</td>
                                </tr>
                                <tr>
                                    <td style="padding: 8px; font-weight: bold;">פרופיל מעוף</td>
                                    <td style="padding: 8px;">הטיל מגיע לשיא הגובה בחצי הדרך למטרה</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </section>
        </main>
    </div>

    <!-- מודאל עריכת משימה -->
    <div id="todoEditModal" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.6); z-index:100000; align-items:center; justify-content:center; padding:20px;">
        <div class="login-card" style="text-align:right; max-width:420px;">
            <h3 style="margin-top:0; color:var(--text-color); font-size:1.15em;">✏️ עריכת משימה</h3>
            <input type="hidden" id="editTodoId">
            
            <label style="font-size:0.85em; font-weight:bold; color:#94a3b8; display:block; margin-bottom:4px;">שם המשימה:</label>
            <input type="text" id="editTodoTitle" class="login-input" style="direction:rtl; text-align:right;" required>
            
            <label style="font-size:0.85em; font-weight:bold; color:#94a3b8; display:block; margin-bottom:4px;">מדריך אחראי:</label>
            <select id="editTodoAssignee" class="login-input" style="direction:rtl; text-align:right;">
                <option value="">👤 ללא שיוך</option>
                <option value="איתי הקר">איתי הקר</option>
                <option value="עדיאל קסה">עדיאל קסה</option>
                <option value="ראם קייזר">ראם קייזר</option>
                <option value="נדב יחיא">נדב יחיא</option>
                <option value="עידו לבקוביץ">עידו לבקוביץ</option>
                <option value="תומר כחלון">תומר כחלון</option>
                <option value="נטע שצברג">נטע שצברג</option>
                <option value="מרקו">מרקו</option>
            </select>
            
            <label style="font-size:0.85em; font-weight:bold; color:#94a3b8; display:block; margin-bottom:4px;">תאריך יעד לביצוע:</label>
            <input type="date" id="editTodoDueDate" class="login-input" style="direction:ltr; text-align:right;">
            
            <div style="display:flex; gap:8px; margin-top:12px;">
                <button type="button" class="login-btn" onclick="saveEditedTodo()">שמור שינויים 💾</button>
                <button type="button" class="login-btn" style="background:#64748b;" onclick="closeEditTodoModal()">ביטול ❌</button>
            </div>
        </div>
    </div>

    <div id="datalistsContainer"></div>

    <script>
        const hebrewDaysShort = ["א'", "ב'", "ג'", "ד'", "ה'", "ו'", "ש'"];
        const monthNames = ["ינואר", "פברואר", "מרץ", "אפריל", "מאי", "יוני", "יולי", "אוגוסט", "ספטמבר", "אוקטובר", "נובמבר", "דצמבר"];
        
        const currentYear = new Date().getFullYear();
        let activeMonth = new Date().getMonth(); 
        let activeDashboardMonth = new Date().getMonth(); 
        let activeWeekIndex = 0; 
        let gorillaChartInstance = null;
        let latestStatusData = {};
        let latestTodosData = {};

        const guidesOptions = ["", "איתי הקר", "עדיאל קסה", "תומר כחלון", "עידו לבקוביץ", "נדב יחיא", "נטע שצברג", "ראם קייזר", "מרקו", "טיפול חודשי", "אחר..."];
        const gorillaOptions = ["", "גורילה 1", "גורילה 2", "גורילה 3", "גורילה 4", "גורילה 5", "גורילה 6", "גורילה 7"];
        const systemsOptions = ["", "ללא", "אחוד", "ישלט", "אחוד סימולטיבי"];

        let memoryData = {
            units: new Set(),
            locations: new Set(),
            contacts: new Set(),
            traineesCount: new Set(["10", "15", "20", "25", "30", "40"]),
            hours: new Set(["08:00 - 13:00", "09:00 - 14:00", "12:00 - 17:00", "08:30 - 15:30"]),
            notes: new Set(["אימון שגרתי תקין", "בוצע שיגור מוצלח", "תדרוך קצינים", "נדרש רענון למשגר", "טיפול חודשי"])
        };

        function getLocalDateString(d = new Date()) {
            const year = d.getFullYear();
            const month = String(d.getMonth() + 1).padStart(2, '0');
            const day = String(d.getDate()).padStart(2, '0');
            return `${year}-${month}-${day}`;
        }

        function getAirForceWeek(date) {
            const d = new Date(date.getFullYear(), date.getMonth(), date.getDate());
            const julyFirst = new Date(currentYear, 6, 1);
            const dayOfWeek = julyFirst.getDay();
            const firstSunday = new Date(currentYear, 6, 1 - dayOfWeek);
            
            const diffTime = d - firstSunday;
            const diffDays = Math.floor(diffTime / (1000 * 60 * 60 * 24));
            const weekOffset = Math.floor(diffDays / 7);
            return 27 + weekOffset;
        }

        let monthWeeksCache = [];
        let allMonthsDataCache = {};

        function debounce(func, wait = 100) {
            let timeout;
            return function(...args) {
                clearTimeout(timeout);
                timeout = setTimeout(() => func.apply(this, args), wait);
            };
        }

        const debouncedFilterSchedule = debounce(filterSchedule, 100);
        const debouncedFilterSlides = debounce(filterSlides, 100);
        const debouncedFilterForms = debounce(filterFormsTab, 100);

        function normalizeRowValues(val) {
            if (Array.isArray(val)) {
                const arr = [...val];
                while (arr.length < 13) arr.push("");
                return arr;
            }
            const arr = Array(13).fill("");
            if (val && typeof val === 'object') {
                Object.keys(val).forEach(k => {
                    const idx = parseInt(k, 10);
                    if (!isNaN(idx) && idx >= 0 && idx < 13) {
                        arr[idx] = val[k] != null ? String(val[k]) : "";
                    }
                });
            }
            return arr;
        }

        window.addEventListener('firebase-ready', () => {
            const savedTab = localStorage.getItem('gorilla_active_tab') || 'schedule';
            const btn = document.querySelector(`.tab-btn[onclick*="${savedTab}"]`);
            if (btn) switchTab(savedTab, { currentTarget: btn }, false);

            const savedTheme = localStorage.getItem('gorilla_theme');
            if (savedTheme === 'dark') {
                document.body.classList.add('dark-mode');
                const tBtn = document.getElementById('themeToggleBtn');
                if (tBtn) tBtn.innerText = '☀️ מצב בהיר';
            }

            initTrainerProfile();
            initMonthFolders();
            initDashboardMonthTabs();
            loadMonthDataFromCloud(activeMonth);
            initCloudStatusSync();
            initCloudTodoSync();
        });

        function loadMonthDataFromCloud(monthIdx) {
            const sheetRef = window.fbRef(window.fbDB, `sheets/${currentYear}_${monthIdx}`);
            window.fbOnValue(sheetRef, (snapshot) => {
                const saved = snapshot.val();
                processLoadedMonthData(monthIdx, saved);
                renderCurrentWeekTables();
                renderDashboard(activeDashboardMonth);
            });
        }

        function processLoadedMonthData(monthIdx, saved) {
            const daysInMonth = new Date(currentYear, monthIdx + 1, 0).getDate();
            let north = [];
            let south = [];
            for (let dayNum = 1; dayNum <= daysInMonth; dayNum++) {
                const dateObj = new Date(currentYear, monthIdx, dayNum);
                const dayOfWeek = dateObj.getDay(); 
                if (dayOfWeek === 5 || dayOfWeek === 6) continue;

                const hDayName = hebrewDaysShort[dayOfWeek];
                let defaultGuideNorth = "איתי הקר";
                let defaultGuideSouth = "עדיאל קסה";

                north.push({ dayNum, hDayName, isWeekend: false, values: ["", defaultGuideNorth, "", "", "", "", "", "", "", "", "", "", ""] });
                south.push({ dayNum, hDayName, isWeekend: false, values: ["", defaultGuideSouth, "", "", "", "", "", "", "", "", "", "", ""] });
            }

            if (saved) {
                if (saved.north && (Array.isArray(saved.north) || typeof saved.north === 'object')) {
                    const northArr = Array.isArray(saved.north) ? saved.north : Object.values(saved.north);
                    north = northArr.filter(item => {
                        const dateObj = new Date(currentYear, monthIdx, item.dayNum);
                        const dow = dateObj.getDay();
                        return dow !== 5 && dow !== 6;
                    }).map(item => {
                        const dateObj = new Date(currentYear, monthIdx, item.dayNum);
                        let defaultGuideNorth = "איתי הקר";
                        let currentVals = normalizeRowValues(item.values);
                        if (!currentVals[1] && !item.hasUserModifiedGuide1) {
                            currentVals[1] = defaultGuideNorth;
                        }
                        return {
                            dayNum: item.dayNum,
                            hDayName: hebrewDaysShort[dateObj.getDay()],
                            isWeekend: false,
                            hasUserModifiedGuide1: item.hasUserModifiedGuide1,
                            values: currentVals
                        };
                    });
                }
                if (saved.south && (Array.isArray(saved.south) || typeof saved.south === 'object')) {
                    const southArr = Array.isArray(saved.south) ? saved.south : Object.values(saved.south);
                    south = southArr.filter(item => {
                        const dateObj = new Date(currentYear, monthIdx, item.dayNum);
                        const dow = dateObj.getDay();
                        return dow !== 5 && dow !== 6;
                    }).map(item => {
                        const dateObj = new Date(currentYear, monthIdx, item.dayNum);
                        let defaultGuideSouth = "עדיאל קסה";
                        let currentVals = normalizeRowValues(item.values);
                        if (!currentVals[1] && !item.hasUserModifiedGuide2) {
                            currentVals[1] = defaultGuideSouth;
                        }
                        return {
                            dayNum: item.dayNum,
                            hDayName: hebrewDaysShort[dateObj.getDay()],
                            isWeekend: false,
                            hasUserModifiedGuide2: item.hasUserModifiedGuide2,
                            values: currentVals
                        };
                    });
                }
            }
            allMonthsDataCache[monthIdx] = { north, south };
            setupWeeksCache(monthIdx);
        }

        function getMonthDataCache(monthIdx) {
            if (!allMonthsDataCache[monthIdx]) {
                processLoadedMonthData(monthIdx, null);
            }
            return allMonthsDataCache[monthIdx];
        }

        function setupWeeksCache(monthIdx) {
            for (let m = 0; m < 12; m++) {
                const mData = getMonthDataCache(m);
                if (mData && mData.north) mData.north.forEach(item => extractMemory(item.values));
                if (mData && mData.south) mData.south.forEach(item => extractMemory(item.values));
            }

            const prevSelectedWeekNum = (monthWeeksCache[activeWeekIndex]) ? monthWeeksCache[activeWeekIndex].weekNum : null;

            const daysInMonth = new Date(currentYear, monthIdx + 1, 0).getDate();
            const weeksMap = new Map();

            for (let dayNum = 1; dayNum <= daysInMonth; dayNum++) {
                const date = new Date(currentYear, monthIdx, dayNum);
                if (date.getDay() === 5 || date.getDay() === 6) continue;

                const wNum = getAirForceWeek(date);
                const dayOfWeek = date.getDay();
                const sunDate = new Date(date);
                sunDate.setDate(date.getDate() - dayOfWeek);

                if (sunDate.getMonth() === monthIdx) {
                    if (!weeksMap.has(wNum)) {
                        const satDate = new Date(sunDate);
                        satDate.setDate(satDate.getDate() + 6);

                        let weekDays = [];
                        for (let d = new Date(sunDate); d <= satDate; d.setDate(d.getDate() + 1)) {
                            if (d.getFullYear() === currentYear && d.getDay() !== 5 && d.getDay() !== 6) {
                                weekDays.push({
                                    month: d.getMonth(),
                                    day: d.getDate(),
                                    hDayName: hebrewDaysShort[d.getDay()],
                                    isWeekend: false
                                });
                            }
                        }
                        if (weekDays.length > 0) {
                            weeksMap.set(wNum, { weekNum: wNum, days: weekDays });
                        }
                    }
                }
            }

            monthWeeksCache = [];
            weeksMap.forEach((wObj) => monthWeeksCache.push(wObj));

            const today = new Date();
            let foundTodayIndex = -1;
            if (currentYear === today.getFullYear()) {
                foundTodayIndex = monthWeeksCache.findIndex(weekObj => 
                    weekObj.days.some(d => d.month === today.getMonth() && d.day === today.getDate())
                );
            }

            if (prevSelectedWeekNum !== null) {
                const foundPrevIndex = monthWeeksCache.findIndex(w => w.weekNum === prevSelectedWeekNum);
                if (foundPrevIndex !== -1) {
                    activeWeekIndex = foundPrevIndex;
                } else if (foundTodayIndex !== -1) {
                    activeWeekIndex = foundTodayIndex;
                } else {
                    activeWeekIndex = 0;
                }
            } else if (foundTodayIndex !== -1) {
                activeWeekIndex = foundTodayIndex;
            } else if (activeWeekIndex >= monthWeeksCache.length) {
                activeWeekIndex = 0;
            }

            rebuildDatalists();
            initWeekTabs();
        }

        function loadMonthData(monthIdx) {
            loadMonthDataFromCloud(monthIdx);
        }

        function extractMemory(vals) {
            if (!vals || !Array.isArray(vals)) return;
            if (vals[2] && vals[2].trim()) memoryData.units.add(vals[2].trim());
            if (vals[3] && vals[3].trim()) memoryData.locations.add(vals[3].trim());
            if (vals[5] && vals[5].trim()) memoryData.contacts.add(vals[5].trim());
            if (vals[6] && vals[6].trim()) memoryData.traineesCount.add(vals[6].trim());
            if (vals[8] && vals[8].trim()) memoryData.hours.add(vals[8].trim());
            if (vals[9] && vals[9].trim()) memoryData.notes.add(vals[9].trim());
        }

        function rebuildDatalists() {
            let container = document.getElementById('datalistsContainer');
            if (!container) return;
            container.innerHTML = `
                <datalist id="mem-units">${Array.from(memoryData.units).map(v => `<option value="${v}">`).join('')}</datalist>
                <datalist id="mem-locations">${Array.from(memoryData.locations).map(v => `<option value="${v}">`).join('')}</datalist>
                <datalist id="mem-contacts">${Array.from(memoryData.contacts).map(v => `<option value="${v}">`).join('')}</datalist>
                <datalist id="mem-count">${Array.from(memoryData.traineesCount).map(v => `<option value="${v}">`).join('')}</datalist>
                <datalist id="mem-hours">${Array.from(memoryData.hours).map(v => `<option value="${v}">`).join('')}</datalist>
                <datalist id="mem-notes">${Array.from(memoryData.notes).map(v => `<option value="${v}">`).join('')}</datalist>
            `;
        }

        function initMonthFolders() {
            const bar = document.getElementById('monthFoldersBar');
            if (!bar) return;
            bar.innerHTML = '';
            monthNames.forEach((mName, idx) => {
                const btn = document.createElement('button');
                btn.className = `month-folder-btn ${idx === activeMonth ? 'active' : ''}`;
                btn.innerText = mName;
                btn.onclick = () => {
                    document.querySelectorAll('#monthFoldersBar .month-folder-btn').forEach(b => b.classList.remove('active'));
                    btn.classList.add('active');
                    activeMonth = idx;
                    activeWeekIndex = 0;
                    loadMonthData(activeMonth);
                };
                bar.appendChild(btn);
            });
        }

        function initDashboardMonthTabs() {
            const bar = document.getElementById('dashboardMonthTabs');
            if (!bar) return;
            bar.innerHTML = '';
            monthNames.forEach((mName, idx) => {
                const btn = document.createElement('button');
                btn.className = `month-folder-btn ${idx === activeDashboardMonth ? 'active' : ''}`;
                btn.innerText = mName;
                btn.onclick = () => {
                    document.querySelectorAll('#dashboardMonthTabs .month-folder-btn').forEach(b => b.classList.remove('active'));
                    btn.classList.add('active');
                    activeDashboardMonth = idx;
                    loadMonthDataFromCloud(activeDashboardMonth);
                    renderDashboard(activeDashboardMonth);
                };
                bar.appendChild(btn);
            });
        }

        function initWeekTabs() {
            const bar = document.getElementById('weekTabsBar');
            if (!bar) return;
            bar.innerHTML = '';
            const today = new Date();

            monthWeeksCache.forEach((weekObj, idx) => {
                const btn = document.createElement('button');
                let isTodayWeek = false;
                if (currentYear === today.getFullYear()) {
                    isTodayWeek = weekObj.days.some(d => d.month === today.getMonth() && d.day === today.getDate());
                }

                const startD = weekObj.days[0];
                const endD = weekObj.days[weekObj.days.length - 1];

                btn.className = `week-tab-btn ${idx === activeWeekIndex ? 'active' : ''} ${isTodayWeek ? 'today-week-tab' : ''}`;
                btn.innerText = `שבוע ${weekObj.weekNum} (${startD.day}/${startD.month+1} - ${endD.day}/${endD.month+1})`;
                btn.onclick = () => {
                    document.querySelectorAll('.week-tab-btn').forEach(b => b.classList.remove('active'));
                    btn.classList.add('active');
                    activeWeekIndex = idx;
                    renderCurrentWeekTables();
                };
                bar.appendChild(btn);
            });
            updateActionButtonsText();
        }

        function updateActionButtonsText() {
            if (monthWeeksCache.length === 0 || !monthWeeksCache[activeWeekIndex]) return;
            const currentWeekObj = monthWeeksCache[activeWeekIndex];
            const btn = document.getElementById('waShiftsBtn');
            if (btn) {
                btn.innerHTML = `<svg viewBox="0 0 24 24" style="width:16px;height:16px;fill:white;flex-shrink:0;"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981zm11.387-5.464c-.074-.124-.272-.198-.57-.347-.297-.149-1.758-.868-2.031-.967-.272-.099-.47-.149-.669.149-.198.297-.768.967-.941 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.521.151-.172.2-.296.3-.495.099-.198.05-.372-.025-.521-.075-.148-.669-1.611-.916-2.206-.242-.579-.487-.501-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.263.489 1.694.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414z"/></svg> שלח משמרות שבוע ${currentWeekObj.weekNum} לוואטסאפ`;
            }
        }

        function renderCurrentWeekTables() {
            const northBody = document.getElementById('northTableBody');
            const southBody = document.getElementById('southTableBody');
            if (!northBody || !southBody) return;

            const activeEl = document.activeElement;
            const activeId = activeEl && activeEl.id ? activeEl.id : null;
            const selStart = (activeEl && activeEl.selectionStart !== undefined) ? activeEl.selectionStart : null;
            const selEnd = (activeEl && activeEl.selectionEnd !== undefined) ? activeEl.selectionEnd : null;

            northBody.innerHTML = '';
            southBody.innerHTML = '';

            if (monthWeeksCache.length === 0 || !monthWeeksCache[activeWeekIndex]) return;
            const currentWeekObj = monthWeeksCache[activeWeekIndex];

            updateActionButtonsText();
            const today = new Date();

            currentWeekObj.days.forEach(dayInfo => {
                const monthData = getMonthDataCache(dayInfo.month);
                const isToday = (currentYear === today.getFullYear() && dayInfo.month === today.getMonth() && dayInfo.day === today.getDate());

                const northRows = monthData.north.filter(item => item.dayNum === dayInfo.day);
                const southRows = monthData.south.filter(item => item.dayNum === dayInfo.day);

                if (northRows.length === 0) {
                    northRows.push({ dayNum: dayInfo.day, values: ["", "איתי הקר", "", "", "", "", "", "", "", "", "", "", ""] });
                }
                if (southRows.length === 0) {
                    southRows.push({ dayNum: dayInfo.day, values: ["", "עדיאל קסה", "", "", "", "", "", "", "", "", "", "", ""] });
                }

                northRows.forEach((nData, index) => {
                    const trNorth = document.createElement('tr');
                    const notes = nData.values[9] || '';
                    const isCanceled = notes.includes('בוטל') || notes.includes('התבטל');

                    if (isToday) trNorth.className = 'today-row';
                    else if (isCanceled) trNorth.className = 'canceled-row';

                    const actualIndex = monthData.north.indexOf(nData);
                    trNorth.innerHTML = buildRowHTML(dayInfo.day, dayInfo.hDayName, nData.values, 'north', dayInfo.month, actualIndex, index > 0);
                    northBody.appendChild(trNorth);
                });

                southRows.forEach((sData, index) => {
                    const trSouth = document.createElement('tr');
                    const notes = sData.values[9] || '';
                    const isCanceled = notes.includes('בוטל') || notes.includes('התבטל');

                    if (isToday) trSouth.className = 'today-row';
                    else if (isCanceled) trSouth.className = 'canceled-row';

                    const actualIndex = monthData.south.indexOf(sData);
                    trSouth.innerHTML = buildRowHTML(dayInfo.day, dayInfo.hDayName, sData.values, 'south', dayInfo.month, actualIndex, index > 0);
                    southBody.appendChild(trSouth);
                });
            });

            document.querySelectorAll('.cell-select').forEach(sel => {
                if (sel.value !== "") sel.classList.add('has-selection');
                else sel.classList.remove('has-selection');
            });

            if (activeId) {
                const restoredEl = document.getElementById(activeId);
                if (restoredEl) {
                    restoredEl.focus();
                    if (selStart !== null && restoredEl.setSelectionRange) {
                        try { restoredEl.setSelectionRange(selStart, selEnd); } catch (e) {}
                    }
                }
            }

            filterSchedule();
        }

        // ================= לוגיקת סנכרון וניהול משימות To-Do =================
        function initCloudTodoSync() {
            const todoRef = window.fbRef(window.fbDB, 'todos');
            window.fbOnValue(todoRef, (snapshot) => {
                latestTodosData = snapshot.val() || {};
                renderTodoList();
                checkUserTodoReminders();
            });
        }

        function getTrainerInitials(name) {
            if (!name) return "??";
            const parts = name.trim().split(/\s+/);
            if (parts.length >= 2) {
                return (parts[0][0] + parts[1][0]).toUpperCase();
            }
            return name.substring(0, 2).toUpperCase();
        }

        function getTrainerColor(name) {
            const colors = ["#0284c7", "#16a34a", "#ea580c", "#9333ea", "#0d9488", "#e11d48", "#d97706", "#4f46e5", "#059669"];
            let hash = 0;
            for (let i = 0; i < (name || '').length; i++) hash = name.charCodeAt(i) + ((hash << 5) - hash);
            return colors[Math.abs(hash) % colors.length];
        }

        function formatTodoDate(dateStr) {
            if (!dateStr) return "";
            const parts = dateStr.split('-');
            if (parts.length === 3) {
                return `${parts[2]}/${parts[1]}`;
            }
            return dateStr;
        }

        // בדיקת תזכורות פנימיות עבור המדריך המחובר (היום ומחר)
        function checkUserTodoReminders() {
            const trainer = JSON.parse(localStorage.getItem('gorilla_trainer_profile') || 'null');
            const banner = document.getElementById('todoUserReminderBanner');
            const bannerText = document.getElementById('todoUserReminderText');
            if (!banner || !bannerText) return;

            if (!trainer || !trainer.firstName) {
                banner.style.display = 'none';
                return;
            }

            const todayStr = getLocalDateString(new Date());
            const tomorrowObj = new Date();
            tomorrowObj.setDate(tomorrowObj.getDate() + 1);
            const tomorrowStr = getLocalDateString(tomorrowObj);

            const tasks = Object.keys(latestTodosData).map(k => ({ id: k, ...latestTodosData[k] }));
            
            let todayTasks = 0;
            let tomorrowTasks = 0;
            let overdueTasks = 0;

            tasks.forEach(t => {
                if (t.completed) return;
                const isAssignedToMe = t.assignee && (t.assignee.includes(trainer.firstName) || (trainer.lastName && t.assignee.includes(trainer.lastName)));
                if (!isAssignedToMe) return;

                if (t.dueDate) {
                    if (t.dueDate < todayStr) overdueTasks++;
                    else if (t.dueDate === todayStr) todayTasks++;
                    else if (t.dueDate === tomorrowStr) tomorrowTasks++;
                }
            });

            const totalUrgent = todayTasks + tomorrowTasks + overdueTasks;
            if (totalUrgent > 0) {
                let msg = `🔔 שלום ${trainer.firstName}, יש לך `;
                let parts = [];
                if (overdueTasks > 0) parts.push(`${overdueTasks} משימות באיחור ⚠️`);
                if (todayTasks > 0) parts.push(`${todayTasks} משימות לביצוע היום ⏰`);
                if (tomorrowTasks > 0) parts.push(`${tomorrowTasks} משימות למחר ⏳`);
                
                msg += parts.join(' | ') + '!';
                bannerText.innerText = msg;
                banner.style.display = 'flex';
            } else {
                banner.style.display = 'none';
            }
        }

        function handleCreateTodo(e) {
            if (e) e.preventDefault();
            const titleInput = document.getElementById('todoTitleInput');
            const assigneeSelect = document.getElementById('todoAssigneeSelect');
            const dateInput = document.getElementById('todoDueDateInput');

            const title = titleInput ? titleInput.value.trim() : "";
            const assignee = assigneeSelect ? assigneeSelect.value : "";
            const dueDate = dateInput ? dateInput.value : "";

            if (!title) return;

            const todoListRef = window.fbRef(window.fbDB, 'todos');
            const newTodoRef = window.fbPush(todoListRef);
            
            const newTodoData = {
                title: title,
                assignee: assignee,
                dueDate: dueDate,
                completed: false,
                starred: false,
                createdAt: Date.now()
            };

            window.fbSet(newTodoRef, newTodoData).then(() => {
                if (titleInput) titleInput.value = "";
                if (dateInput) dateInput.value = "";
            }).catch(console.error);
        }

        window.toggleTodoCompleted = function(id, currentStatus) {
            const updates = {};
            updates[`todos/${id}/completed`] = !currentStatus;
            window.fbUpdate(window.fbRef(window.fbDB), updates).catch(console.error);
        };

        window.toggleTodoStarred = function(id, currentStatus) {
            const updates = {};
            updates[`todos/${id}/starred`] = !currentStatus;
            window.fbUpdate(window.fbRef(window.fbDB), updates).catch(console.error);
        };

        window.deleteTodo = function(id) {
            if (!confirm("האם למחוק משימה זו?")) return;
            const itemRef = window.fbRef(window.fbDB, `todos/${id}`);
            window.fbRemove(itemRef).catch(console.error);
        };

        // פונקציות עריכת משימה
        window.openEditTodoModal = function(id) {
            const task = latestTodosData[id];
            if (!task) return;

            document.getElementById('editTodoId').value = id;
            document.getElementById('editTodoTitle').value = task.title || '';
            document.getElementById('editTodoAssignee').value = task.assignee || '';
            document.getElementById('editTodoDueDate').value = task.dueDate || '';

            const modal = document.getElementById('todoEditModal');
            if (modal) modal.style.display = 'flex';
        };

        window.closeEditTodoModal = function() {
            const modal = document.getElementById('todoEditModal');
            if (modal) modal.style.display = 'none';
        };

        window.saveEditedTodo = function() {
            const id = document.getElementById('editTodoId').value;
            const title = document.getElementById('editTodoTitle').value.trim();
            const assignee = document.getElementById('editTodoAssignee').value;
            const dueDate = document.getElementById('editTodoDueDate').value;

            if (!id || !title) {
                alert('נא להזין כותרת למשימה.');
                return;
            }

            const updates = {};
            updates[`todos/${id}/title`] = title;
            updates[`todos/${id}/assignee`] = assignee;
            updates[`todos/${id}/dueDate`] = dueDate;

            window.fbUpdate(window.fbRef(window.fbDB), updates).then(() => {
                closeEditTodoModal();
            }).catch(console.error);
        };

        function renderTodoList() {
            const activeContainer = document.getElementById('activeTodoList');
            const completedContainer = document.getElementById('completedTodoList');
            const completedSection = document.getElementById('completedTodoSection');
            const countDisplay = document.getElementById('todoCountDisplay');
            const completedCountDisplay = document.getElementById('completedCountDisplay');

            if (!activeContainer) return;

            activeContainer.innerHTML = '';
            if (completedContainer) completedContainer.innerHTML = '';

            const tasks = Object.keys(latestTodosData).map(k => ({ id: k, ...latestTodosData[k] }));

            // מיון: מכוכבים קודם, ולאחר מכן לפי תאריך יצירה
            tasks.sort((a, b) => {
                if (a.starred && !b.starred) return -1;
                if (!a.starred && b.starred) return 1;
                return (b.createdAt || 0) - (a.createdAt || 0);
            });

            const activeTasks = tasks.filter(t => !t.completed);
            const completedTasks = tasks.filter(t => t.completed);

            if (countDisplay) countDisplay.innerText = `${activeTasks.length} משימות פתוחות`;
            if (completedCountDisplay) completedCountDisplay.innerText = completedTasks.length;

            if (activeTasks.length === 0) {
                activeContainer.innerHTML = `<div style="text-align:center; padding:20px; color:#94a3b8; font-size:0.9em;">אין משימות פתוחות כרגע. כל הכבוד! 🎉</div>`;
            } else {
                activeTasks.forEach(task => {
                    activeContainer.appendChild(buildTodoItemElement(task));
                });
            }

            if (completedTasks.length > 0 && completedContainer && completedSection) {
                completedSection.style.display = 'block';
                completedTasks.forEach(task => {
                    completedContainer.appendChild(buildTodoItemElement(task));
                });
            } else if (completedSection) {
                completedSection.style.display = 'none';
            }
        }

        function buildTodoItemElement(task) {
            const card = document.createElement('div');
            // אם המשימה מסומנת בכוכב - מקבלת class 'starred' לצביעה בצהוב
            card.className = `todo-item-card ${task.completed ? 'completed' : ''} ${task.starred ? 'starred' : ''}`;

            const initials = task.assignee ? getTrainerInitials(task.assignee) : "";
            const avatarBg = task.assignee ? getTrainerColor(task.assignee) : "#64748b";

            const assigneeBadge = task.assignee ? `
                <div class="trainer-badge-avatar" style="background-color: ${avatarBg};" title="אחראי: ${task.assignee}">
                    ${initials}
                </div>
            ` : '';

            // חישוב תאריך: איחור (אדום עם !), היום, מחר או תאריך רגיל
            let dateBadge = '';
            if (task.dueDate) {
                const todayStr = getLocalDateString(new Date());
                const tomorrowObj = new Date();
                tomorrowObj.setDate(tomorrowObj.getDate() + 1);
                const tomorrowStr = getLocalDateString(tomorrowObj);
                const formattedDate = formatTodoDate(task.dueDate);

                if (task.dueDate < todayStr && !task.completed) {
                    dateBadge = `<div class="todo-item-date overdue"><span style="color:#ef4444; font-weight:900; font-size:1.15em;">!</span> 📅 ${formattedDate} (באיחור)</div>`;
                } else if (task.dueDate === todayStr && !task.completed) {
                    dateBadge = `<div class="todo-item-date due-today">⏰ היום (${formattedDate})</div>`;
                } else if (task.dueDate === tomorrowStr && !task.completed) {
                    dateBadge = `<div class="todo-item-date due-tomorrow">⏳ מחר (${formattedDate})</div>`;
                } else {
                    dateBadge = `<div class="todo-item-date">📅 ${formattedDate}</div>`;
                }
            }

            card.innerHTML = `
                <div class="todo-main-content">
                    <button type="button" class="todo-check-btn ${task.completed ? 'checked' : ''}" onclick="toggleTodoCompleted('${task.id}', ${task.completed})" title="${task.completed ? 'סמן כלא הושלם' : 'סמן כהושלם'}">
                        ${task.completed ? '✓' : ''}
                    </button>
                    <div class="todo-item-info">
                        <div class="todo-item-title">${task.title}</div>
                        ${dateBadge}
                    </div>
                </div>
                <div class="todo-actions-right">
                    ${assigneeBadge}
                    <button type="button" class="todo-edit-btn" onclick="openEditTodoModal('${task.id}')" title="ערוך משימה">✏️</button>
                    <button type="button" class="todo-star-btn ${task.starred ? 'starred' : ''}" onclick="toggleTodoStarred('${task.id}', ${task.starred})" title="סמן בכוכב">
                        ${task.starred ? '★' : '☆'}
                    </button>
                    <button type="button" class="todo-delete-btn" onclick="deleteTodo('${task.id}')" title="מחק משימה">🗑️</button>
                </div>
            `;
            return card;
        }

        // ================= רינדור דשבורד =================
        function renderDashboard(monthIdx) {
            const monthName = monthNames[monthIdx];
            const titleEl = document.getElementById('statsMonthTitle');
            const chartMonthLabel = document.getElementById('chartMonthLabel');
            if (titleEl) titleEl.innerText = `${monthName} ${currentYear}`;
            if (chartMonthLabel) chartMonthLabel.innerText = `(חודש ${monthName})`;

            let healthyCount = 0;
            let faultyCount = 0;
            let faultsList = [];
            const today = new Date();

            let cleaningDaysArray = [];
            for (let i = 0; i < 7; i++) {
                const row = latestStatusData[i] || {};
                const status = row.status || (i === 1 || i === 3 || i === 6 ? 'לא תקין' : 'תקין');
                if (status === 'תקין') healthyCount++;
                else {
                    faultyCount++;
                    faultsList.push({
                        gorillaName: `גורילה מס ${i + 1}`,
                        notes: row.notes || 'תקלה לא פורטה'
                    });
                }

                let daysSince = 0;
                if (row.cleaning) {
                    const cleanDate = new Date(row.cleaning);
                    const diffTime = today - cleanDate;
                    daysSince = Math.max(0, Math.floor(diffTime / (1000 * 60 * 60 * 24)));
                } else {
                    daysSince = 16;
                }
                cleaningDaysArray.push(daysSince);
            }

            const kpiHealthy = document.getElementById('kpiHealthyGorillas');
            const kpiFaulty = document.getElementById('kpiFaultyGorillas');
            if (kpiHealthy) kpiHealthy.innerText = healthyCount;
            if (kpiFaulty) kpiFaulty.innerText = faultyCount;

            const faultsContainer = document.getElementById('openFaultsContainer');
            const faultsBadge = document.getElementById('faultsCountBadge');
            if (faultsBadge) faultsBadge.innerText = `${faultyCount} תקלות פתוחות`;

            if (faultsContainer) {
                if (faultsList.length === 0) {
                    faultsContainer.innerHTML = `<div style="color: #22c55e; font-weight: bold; padding: 10px; text-align: center;">כל המאמנים תקינים כעת! ✓</div>`;
                } else {
                    faultsContainer.innerHTML = faultsList.map(f => `
                        <div class="fault-row-item">
                            <span>${f.notes}</span>
                            <span style="font-weight: 800;">${f.gorillaName}</span>
                        </div>
                    `).join('');
                }
            }

            const monthData = getMonthDataCache(monthIdx);
            let activeTrainingDays = new Set();
            let canceledTrainingDays = new Set();
            let totalTrainees = 0;
            let totalHours = 0;
            let uniqueLocations = new Set();
            let uniqueUnits = new Set();
            let gorillaTrainingDays = [0, 0, 0, 0, 0, 0, 0];

            const processRows = (rows) => {
                rows.forEach(item => {
                    const vals = item.values || [];
                    const notes = vals[9] || '';
                    const isCanceled = notes.includes('בוטל') || notes.includes('התבטל');

                    if (isCanceled) {
                        canceledTrainingDays.add(item.dayNum);
                        return;
                    }

                    const hasGuide = vals[1] && vals[1].trim() !== "";
                    const hasUnit = vals[2] && vals[2].trim() !== "" && vals[2].trim() !== "ללא";
                    const hasLocation = vals[3] && vals[3].trim() !== "";

                    const isFullTrainingDay = hasGuide && hasUnit && hasLocation;

                    if (isFullTrainingDay) {
                        activeTrainingDays.add(item.dayNum);
                    }

                    if (hasUnit) uniqueUnits.add(vals[2].trim());
                    if (hasLocation) uniqueLocations.add(vals[3].trim());

                    if (vals[6] && !isNaN(parseInt(vals[6]))) {
                        totalTrainees += parseInt(vals[6]);
                    }

                    if (vals[8] && vals[8].trim()) {
                        totalHours += 5;
                    }

                    for (let g = 1; g <= 7; g++) {
                        const gName = `גורילה ${g}`;
                        const gNameAlt = `גורילה מס ${g}`;
                        if ((vals[7] && (vals[7].includes(gName) || vals[7].includes(gNameAlt))) ||
                            (vals[11] && (vals[11].includes(gName) || vals[11].includes(gNameAlt)))) {
                            if (isFullTrainingDay) {
                                gorillaTrainingDays[g - 1]++;
                            }
                        }
                    }
                });
            };

            processRows(monthData.north);
            processRows(monthData.south);

            const kpiDays = document.getElementById('kpiMonthTrainingDays');
            const kpiCanceled = document.getElementById('kpiMonthCanceledDays');
            if (kpiDays) kpiDays.innerText = activeTrainingDays.size;
            if (kpiCanceled) kpiCanceled.innerText = canceledTrainingDays.size;

            const dashTrainees = document.getElementById('dashTotalTrainees');
            if (dashTrainees) dashTrainees.innerText = `${totalTrainees} מתאמנים`;

            const dashHours = document.getElementById('dashTotalHours');
            if (dashHours) dashHours.innerText = `${totalHours} שעות פעילות`;

            const locList = document.getElementById('dashLocationsList');
            if (locList) {
                locList.innerHTML = uniqueLocations.size > 0 
                    ? Array.from(uniqueLocations).map(l => `<span class="info-tag">${l}</span>`).join('') 
                    : '<span style="color:#64748b; font-size:0.85em;">אין מיקומים רשומים</span>';
            }

            const unitsList = document.getElementById('dashUnitsList');
            if (unitsList) {
                unitsList.innerHTML = uniqueUnits.size > 0 
                    ? Array.from(uniqueUnits).map(u => `<span class="info-tag">${u}</span>`).join('') 
                    : '<span style="color:#64748b; font-size:0.85em;">אין יחידות רשומות</span>';
            }

            updateGorillaBarChart(cleaningDaysArray, gorillaTrainingDays);
        }

        function updateGorillaBarChart(cleaningDays, trainingDays) {
            const ctx = document.getElementById('gorillaBarChart');
            if (!ctx) return;

            const isDark = document.body.classList.contains('dark-mode');
            const labels = ['גורילה מס 1', 'גורילה מס 2', 'גורילה מס 3', 'גורילה מס 4', 'גורילה מס 5', 'גורילה מס 6', 'גורילה מס 7'];

            if (gorillaChartInstance) {
                gorillaChartInstance.destroy();
            }

            gorillaChartInstance = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: labels,
                    datasets: [
                        {
                            label: 'ימים מאז טיפול אחרון',
                            data: cleaningDays,
                            backgroundColor: '#22c55e',
                            borderRadius: 6,
                            borderSkipped: false
                        },
                        {
                            label: 'ימי אימון בחודש',
                            data: trainingDays,
                            backgroundColor: '#0284c7',
                            borderRadius: 6,
                            borderSkipped: false
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    interaction: { mode: 'index', intersect: false },
                    plugins: {
                        legend: {
                            position: 'bottom',
                            labels: {
                                color: isDark ? '#f8fafc' : '#2c3e50',
                                font: { family: 'Segoe UI', weight: 'bold', size: 11 }
                            }
                        },
                        tooltip: {
                            rtl: true,
                            backgroundColor: 'rgba(15, 23, 42, 0.9)',
                            titleFont: { family: 'Segoe UI', size: 12, weight: 'bold' },
                            bodyFont: { family: 'Segoe UI', size: 12 },
                            padding: 10,
                            boxPadding: 4,
                            callbacks: {
                                label: function(context) {
                                    return ` ${context.dataset.label}: ${context.raw}`;
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            grid: { display: false },
                            ticks: {
                                color: isDark ? '#94a3b8' : '#64748b',
                                font: { family: 'Segoe UI', size: 10, weight: 'bold' }
                            }
                        },
                        y: {
                            beginAtZero: true,
                            grid: { color: isDark ? 'rgba(255,255,255,0.06)' : 'rgba(0,0,0,0.06)' },
                            ticks: {
                                color: isDark ? '#94a3b8' : '#64748b',
                                font: { family: 'Segoe UI', size: 10 }
                            }
                        }
                    }
                }
            });
        }

        function addExtraRow(side) {
            if (monthWeeksCache.length === 0 || !monthWeeksCache[activeWeekIndex]) return;
            const currentWeekObj = monthWeeksCache[activeWeekIndex];

            const weekDaysOnly = currentWeekObj.days.filter(d => {
                const dateObj = new Date(currentYear, d.month, d.day);
                const dayOfWeek = dateObj.getDay();
                return dayOfWeek !== 5 && dayOfWeek !== 6;
            });

            if (weekDaysOnly.length === 0) {
                alert("אין ימי חול זמינים בשבוע זה.");
                return;
            }

            let promptMsg = "בחר תאריך מתוך ימי החול בשבוע הנוכחי להוספת שורה:\n\n";
            weekDaysOnly.forEach((d, idx) => {
                promptMsg += `${idx + 1}) יום ${d.hDayName} (${String(d.day).padStart(2, '0')}.${String(d.month + 1).padStart(2, '0')})\n`;
            });
            promptMsg += "\nהקלד את מספר היום ברשימה (1-5) או את תאריך היום בחודש:";

            let input = prompt(promptMsg);
            if (!input) return;
            input = input.trim();

            let targetDayInfo = null;
            let choiceIndex = parseInt(input);

            if (!isNaN(choiceIndex) && choiceIndex >= 1 && choiceIndex <= weekDaysOnly.length) {
                targetDayInfo = weekDaysOnly[choiceIndex - 1];
            } else {
                let dayNumInput = parseInt(input.split('.')[0]);
                targetDayInfo = weekDaysOnly.find(d => d.day === dayNumInput);
            }

            if (!targetDayInfo) {
                alert("תאריך לא תקין, נבחר יום בסוף שבוע, או שהיום אינו מופיע בשבוע זה.");
                return;
            }

            let dayNum = targetDayInfo.day;
            let targetMonthIdx = targetDayInfo.month;

            const monthData = getMonthDataCache(targetMonthIdx);
            const dateStr = `${String(dayNum).padStart(2, '0')}.${String(targetMonthIdx + 1).padStart(2, '0')}`;
            const dateObj = new Date(currentYear, targetMonthIdx, dayNum);
            const hDayName = hebrewDaysShort[dateObj.getDay()];
            const defGuide = side === 'north' ? "איתי הקר" : "עדיאל קסה";
            const newValues = [`${dateStr} ${hDayName}`, defGuide, "", "", "", "", "", "", "", "", "", "", ""];

            const newRow = {
                dayNum: dayNum,
                hDayName: hDayName,
                isWeekend: false,
                values: newValues
            };

            if (side === 'north') {
                monthData.north.push(newRow);
                monthData.north.sort((a, b) => a.dayNum - b.dayNum);
            } else {
                monthData.south.push(newRow);
                monthData.south.sort((a, b) => a.dayNum - b.dayNum);
            }

            saveSideArrayToCloud(side, targetMonthIdx);
            renderCurrentWeekTables();
            renderDashboard(activeDashboardMonth);
        }

        function removeExtraRow(side, monthIdx, cacheIndex) {
            if (!confirm("האם אתה בטוח שברצונך למחוק שורה זו?")) return;
            const monthData = getMonthDataCache(monthIdx);
            if (side === 'north') {
                monthData.north.splice(cacheIndex, 1);
            } else {
                monthData.south.splice(cacheIndex, 1);
            }
            saveSideArrayToCloud(side, monthIdx);
            renderCurrentWeekTables();
            renderDashboard(activeDashboardMonth);
        }

        function showSecondGuideSelect(side, monthIdx, cacheIndex) {
            const monthData = getMonthDataCache(monthIdx);
            const rowData = side === 'north' ? monthData.north[cacheIndex] : monthData.south[cacheIndex];
            if (rowData) {
                if (!rowData.values[10]) {
                    rowData.values[10] = guidesOptions[1] || "";
                    updateCacheAndSave(side, monthIdx, cacheIndex, 10, rowData.values[10]);
                }
            }
            renderCurrentWeekTables();
        }

        function removeSecondGuideSelect(side, monthIdx, cacheIndex) {
            updateCacheAndSave(side, monthIdx, cacheIndex, 10, "");
            renderCurrentWeekTables();
        }

        function showSecondGorillaSelect(side, monthIdx, cacheIndex) {
            const monthData = getMonthDataCache(monthIdx);
            const rowData = side === 'north' ? monthData.north[cacheIndex] : monthData.south[cacheIndex];
            if (rowData) {
                if (!rowData.values[11]) {
                    rowData.values[11] = gorillaOptions[1] || "גורילה 1";
                    updateCacheAndSave(side, monthIdx, cacheIndex, 11, rowData.values[11]);
                }
            }
            renderCurrentWeekTables();
        }

        function removeSecondGorillaSelect(side, monthIdx, cacheIndex) {
            updateCacheAndSave(side, monthIdx, cacheIndex, 11, "");
            renderCurrentWeekTables();
        }

        window.handleGuideSelection = function(side, monthIdx, cacheIndex, fieldIndex, selectEl) {
            let val = selectEl.value;
            if (val === "אחר...") {
                let customName = prompt("הזן את שם המדריך:");
                if (customName && customName.trim() !== "") {
                    val = customName.trim();
                } else {
                    selectEl.value = "";
                    val = "";
                }
            }
            handleSelectChange(selectEl);

            const monthData = getMonthDataCache(monthIdx);
            const row = side === 'north' ? monthData.north[cacheIndex] : monthData.south[cacheIndex];

            if (row) {
                if (!Array.isArray(row.values)) row.values = Array(13).fill("");
                while (row.values.length < 13) row.values.push("");

                row.values[fieldIndex] = val;
                const updates = {};
                updates[`sheets/${currentYear}_${monthIdx}/${side}/${cacheIndex}/values/${fieldIndex}`] = val;

                if (fieldIndex === 1) {
                    if (side === 'north') {
                        row.hasUserModifiedGuide1 = true;
                        updates[`sheets/${currentYear}_${monthIdx}/north/${cacheIndex}/hasUserModifiedGuide1`] = true;
                    } else {
                        row.hasUserModifiedGuide2 = true;
                        updates[`sheets/${currentYear}_${monthIdx}/south/${cacheIndex}/hasUserModifiedGuide2`] = true;
                    }

                    if (window.trainerGorillaMap[val]) {
                        const defaults = window.trainerGorillaMap[val];
                        row.values[7] = defaults[0];
                        updates[`sheets/${currentYear}_${monthIdx}/${side}/${cacheIndex}/values/7`] = defaults[0];

                        if (defaults[1]) {
                            row.values[11] = defaults[1];
                            updates[`sheets/${currentYear}_${monthIdx}/${side}/${cacheIndex}/values/11`] = defaults[1];
                        }
                    }
                }

                window.fbUpdate(window.fbRef(window.fbDB), updates).catch(console.error);
                extractMemory(row.values);
                rebuildDatalists();
            }

            renderCurrentWeekTables();
            renderDashboard(activeDashboardMonth);
        };

        function buildRowHTML(dayNum, hDayName, vals, side, monthIdx, cacheIndex, isExtra) {
            const dateStr = `${String(dayNum).padStart(2, '0')}.${String(monthIdx + 1).padStart(2, '0')}`;
            const currentVal = vals[0] || `${dateStr} ${hDayName}`;
            const extraBadge = isExtra ? `<div style="font-size:0.7em; color:#e74c3c; font-weight:600; margin-top:1px; cursor:pointer;" onclick="removeExtraRow('${side}', ${monthIdx}, ${cacheIndex})" title="לחץ למחיקת השורה">❌ (נוסף)</div>` : '';

            const guide1Val = vals[1] || '';
            const guide2Val = vals[10] || '';
            const hasGuide1 = guide1Val.trim() !== '';
            const hasGuide2 = guide2Val.trim() !== '';

            let localGuides1 = [...guidesOptions];
            if (guide1Val && !localGuides1.includes(guide1Val)) {
                localGuides1.splice(localGuides1.length - 1, 0, guide1Val);
            }

            let localGuides2 = [...guidesOptions];
            if (guide2Val && !localGuides2.includes(guide2Val)) {
                localGuides2.splice(localGuides2.length - 1, 0, guide2Val);
            }

            let guideCellHTML = `
                <td>
                    <div class="guides-container">
                        <div class="guide-row-flex">
                            <select id="cell_${side}_${monthIdx}_${cacheIndex}_1" class="cell-select ${guide1Val ? 'has-selection' : ''}" onchange="handleGuideSelection('${side}', ${monthIdx}, ${cacheIndex}, 1, this)">
                                ${localGuides1.map(g => `<option value="${g}" ${guide1Val === g ? 'selected' : ''}>${g}</option>`).join('')}
                            </select>
                            ${hasGuide1 && !hasGuide2 ? `<button type="button" class="add-guide-btn" onclick="showSecondGuideSelect('${side}', ${monthIdx}, ${cacheIndex})" title="הוסף מדריך נוסף">➕</button>` : ''}
                        </div>
                        ${hasGuide2 ? `
                        <div class="guide-row-flex">
                            <select id="cell_${side}_${monthIdx}_${cacheIndex}_10" class="cell-select ${guide2Val ? 'has-selection' : ''}" onchange="handleGuideSelection('${side}', ${monthIdx}, ${cacheIndex}, 10, this)">
                                ${localGuides2.map(g => `<option value="${g}" ${guide2Val === g ? 'selected' : ''}>${g}</option>`).join('')}
                            </select>
                            <button type="button" class="remove-guide-btn" onclick="removeSecondGuideSelect('${side}', ${monthIdx}, ${cacheIndex})" title="הסר מדריך שני">❌</button>
                        </div>
                        ` : ''}
                    </div>
                </td>
            `;

            const gorilla1Val = vals[7] || '';
            const gorilla2Val = vals[11] || '';
            const hasGorilla1 = gorilla1Val.trim() !== '';
            const hasGorilla2 = gorilla2Val.trim() !== '';

            let gorillaCellHTML = `
                <td>
                    <div class="gorillas-container">
                        <div class="gorilla-row-flex">
                            <select id="cell_${side}_${monthIdx}_${cacheIndex}_7" class="cell-select ${gorilla1Val ? 'has-selection' : ''}" onchange="handleSelectChange(this); updateCacheAndSave('${side}', ${monthIdx}, ${cacheIndex}, 7, this.value); renderCurrentWeekTables();">
                                ${gorillaOptions.map(g => `<option value="${g}" ${gorilla1Val === g ? 'selected' : ''}>${g}</option>`).join('')}
                            </select>
                            ${hasGorilla1 && !hasGorilla2 ? `<button type="button" class="add-gorilla-btn" onclick="showSecondGorillaSelect('${side}', ${monthIdx}, ${cacheIndex})" title="הוסף גורילה נוספת">➕</button>` : ''}
                        </div>
                        ${hasGorilla2 ? `
                        <div class="gorilla-row-flex">
                            <select id="cell_${side}_${monthIdx}_${cacheIndex}_11" class="cell-select ${gorilla2Val ? 'has-selection' : ''}" onchange="handleSelectChange(this); updateCacheAndSave('${side}', ${monthIdx}, ${cacheIndex}, 11, this.value)">
                                ${gorillaOptions.map(g => `<option value="${g}" ${gorilla2Val === g ? 'selected' : ''}>${g}</option>`).join('')}
                            </select>
                            <button type="button" class="remove-gorilla-btn" onclick="removeSecondGorillaSelect('${side}', ${monthIdx}, ${cacheIndex})" title="הסר גורילה שנייה">❌</button>
                        </div>
                        ` : ''}
                    </div>
                </td>
            `;

            return `
                <td>
                    <input id="cell_${side}_${monthIdx}_${cacheIndex}_0" type="text" class="cell-input" value="${currentVal}" onchange="updateCacheAndSave('${side}', ${monthIdx}, ${cacheIndex}, 0, this.value)">
                    ${extraBadge}
                </td>
                ${guideCellHTML}
                <td><input id="cell_${side}_${monthIdx}_${cacheIndex}_2" type="text" class="cell-input" value="${vals[2] || ''}" placeholder="כוח מתאמן" list="mem-units" onchange="updateCacheAndSave('${side}', ${monthIdx}, ${cacheIndex}, 2, this.value)"></td>
                <td><input id="cell_${side}_${monthIdx}_${cacheIndex}_3" type="text" class="cell-input" value="${vals[3] || ''}" placeholder="מיקום" list="mem-locations" onchange="updateCacheAndSave('${side}', ${monthIdx}, ${cacheIndex}, 3, this.value)"></td>
                <td>
                    <select id="cell_${side}_${monthIdx}_${cacheIndex}_4" class="cell-select ${vals[4] ? 'has-selection' : ''}" onchange="handleSelectChange(this); updateCacheAndSave('${side}', ${monthIdx}, ${cacheIndex}, 4, this.value)">
                        ${systemsOptions.map(s => `<option value="${s}" ${vals[4] === s ? 'selected' : ''}>${s}</option>`).join('')}
                    </select>
                </td>
                <td><input id="cell_${side}_${monthIdx}_${cacheIndex}_5" type="text" class="cell-input" value="${vals[5] || ''}" placeholder="איש קשר" list="mem-contacts" onchange="updateCacheAndSave('${side}', ${monthIdx}, ${cacheIndex}, 5, this.value)"></td>
                <td><input id="cell_${side}_${monthIdx}_${cacheIndex}_6" type="text" class="cell-input" value="${vals[6] || ''}" placeholder="מס'" list="mem-count" onchange="updateCacheAndSave('${side}', ${monthIdx}, ${cacheIndex}, 6, this.value)"></td>
                ${gorillaCellHTML}
                <td><input id="cell_${side}_${monthIdx}_${cacheIndex}_8" type="text" class="cell-input" value="${vals[8] || ''}" placeholder="שעות" list="mem-hours" onchange="updateCacheAndSave('${side}', ${monthIdx}, ${cacheIndex}, 8, this.value)"></td>
                <td><input id="cell_${side}_${monthIdx}_${cacheIndex}_9" type="text" class="cell-input" value="${vals[9] || ''}" placeholder="הערות" list="mem-notes" onchange="handleNotesChange('${side}', ${monthIdx}, ${cacheIndex}, this.value)"></td>
                <td><input id="cell_${side}_${monthIdx}_${cacheIndex}_12" type="text" class="cell-input" value="${vals[12] || ''}" placeholder="ניידת" onchange="updateCacheAndSave('${side}', ${monthIdx}, ${cacheIndex}, 12, this.value)"></td>
            `;
        }

        function handleSelectChange(selectEl) {
            if (selectEl.value !== "") selectEl.classList.add('has-selection');
            else selectEl.classList.remove('has-selection');
        }

        function handleNotesChange(side, monthIdx, cacheIndex, value) {
            updateCacheAndSave(side, monthIdx, cacheIndex, 9, value);
            
            if (value && value.trim().includes("טיפול חודשי")) {
                updateCacheAndSave(side, monthIdx, cacheIndex, 2, "טיפול חודשי");
            }
            
            renderCurrentWeekTables();
            renderDashboard(activeDashboardMonth);
        }

        function updateCacheAndSave(side, monthIdx, cacheIndex, fieldIndex, value) {
            const monthData = getMonthDataCache(monthIdx);
            const targetRow = side === 'north' ? monthData.north[cacheIndex] : monthData.south[cacheIndex];

            if (targetRow) {
                if (!Array.isArray(targetRow.values)) targetRow.values = Array(13).fill("");
                while (targetRow.values.length < 13) targetRow.values.push("");

                targetRow.values[fieldIndex] = value;
                
                const updates = {};
                updates[`sheets/${currentYear}_${monthIdx}/${side}/${cacheIndex}/values/${fieldIndex}`] = value;

                if (fieldIndex === 1) {
                    if (side === 'north') {
                        targetRow.hasUserModifiedGuide1 = true;
                        updates[`sheets/${currentYear}_${monthIdx}/north/${cacheIndex}/hasUserModifiedGuide1`] = true;
                    } else {
                        targetRow.hasUserModifiedGuide2 = true;
                        updates[`sheets/${currentYear}_${monthIdx}/south/${cacheIndex}/hasUserModifiedGuide2`] = true;
                    }
                }

                window.fbUpdate(window.fbRef(window.fbDB), updates).catch(console.error);

                extractMemory(targetRow.values);
                rebuildDatalists();
                renderDashboard(activeDashboardMonth);
            }
        }

        function saveSideArrayToCloud(side, monthIdx) {
            const monthData = getMonthDataCache(monthIdx);
            const cleanArray = monthData[side].map(item => ({
                dayNum: item.dayNum,
                values: normalizeRowValues(item.values),
                hasUserModifiedGuide1: !!item.hasUserModifiedGuide1,
                hasUserModifiedGuide2: !!item.hasUserModifiedGuide2
            }));

            const sideRef = window.fbRef(window.fbDB, `sheets/${currentYear}_${monthIdx}/${side}`);
            window.fbSet(sideRef, cleanArray).catch(console.error);
        }

        function initCloudStatusSync() {
            const statusRef = window.fbRef(window.fbDB, 'gorilla_statuses');
            window.fbOnValue(statusRef, (snapshot) => {
                const data = snapshot.val();
                latestStatusData = data || {};
                const todayDateStr = new Date().toISOString().split('T')[0];
                const statusRows = document.querySelectorAll('#statusTableBody tr');
                
                statusRows.forEach((row, index) => {
                    const statusSelect = row.querySelector('.status-select');
                    const cleaningInput = row.querySelector('.cleaning-date-input');
                    const cleaningBtn = row.querySelector('.cleaning-today-btn');
                    const notesInput = row.querySelector('.notes-input');
                    const nameCell = row.querySelector('.gorilla-name-cell');

                    const rowData = data && data[index] ? data[index] : null;

                    if (rowData) {
                        if (document.activeElement !== statusSelect) statusSelect.value = rowData.status || 'תקין';
                        if (document.activeElement !== cleaningInput && cleaningInput) {
                            cleaningInput.value = rowData.cleaning || todayDateStr;
                            updateCleaningButtonText(cleaningBtn, cleaningInput.value);
                        }
                        if (document.activeElement !== notesInput && notesInput) {
                            notesInput.value = rowData.notes !== undefined ? rowData.notes : '';
                        }
                    } else {
                        if (document.activeElement !== cleaningInput && cleaningInput) {
                            cleaningInput.value = todayDateStr;
                            updateCleaningButtonText(cleaningBtn, todayDateStr);
                        }
                    }

                    if (statusSelect && statusSelect.value === 'לא תקין') {
                        if (nameCell) { nameCell.style.background = '#e74c3c'; nameCell.style.color = 'white'; }
                        if (notesInput) { notesInput.style.color = '#e74c3c'; notesInput.style.fontWeight = 'bold'; }
                    } else {
                        if (nameCell) { nameCell.style.background = '#27ae60'; nameCell.style.color = 'white'; }
                        if (notesInput) { notesInput.style.color = ''; notesInput.style.fontWeight = ''; }
                    }
                });

                renderDashboard(activeDashboardMonth);
            });
        }

        function saveStatusData() {
            const rows = document.querySelectorAll('#statusTableBody tr');
            let statusesData = {};
            rows.forEach((row, index) => {
                const statusSelect = row.querySelector('.status-select');
                const cleaningInput = row.querySelector('.cleaning-date-input');
                const notesInput = row.querySelector('.notes-input');
                statusesData[index] = {
                    status: statusSelect ? statusSelect.value : 'תקין',
                    cleaning: cleaningInput ? cleaningInput.value : '',
                    notes: notesInput ? notesInput.value : ''
                };
            });
            latestStatusData = statusesData;
            const statusRef = window.fbRef(window.fbDB, 'gorilla_statuses');
            window.fbSet(statusRef, statusesData);
            renderDashboard(activeDashboardMonth);
        }

        function openCleaningPicker(btn) {
            const row = btn.closest('tr');
            const input = row.querySelector('.cleaning-date-input');
            if (input) {
                if (typeof input.showPicker === 'function') input.showPicker();
                else input.click();
            }
        }

        function onCleaningDateChange(input) {
            const row = input.closest('tr');
            const btn = row.querySelector('.cleaning-today-btn');
            if (input.value) updateCleaningButtonText(btn, input.value);
            saveStatusData();
        }

        function updateCleaningButtonText(btn, dateStr) {
            if (!dateStr || !btn) return;
            const parts = dateStr.split('-');
            if (parts.length === 3) btn.innerText = `${parts[2]}/${parts[1]}`;
        }

        window.initTrainerProfile = function(currentUser) {
            let trainer = JSON.parse(localStorage.getItem('gorilla_trainer_profile') || 'null');
            
            if (!trainer && currentUser && currentUser.email) {
                const emailKey = currentUser.email.toLowerCase();
                if (window.knownTrainers && window.knownTrainers[emailKey]) {
                    trainer = {
                        firstName: window.knownTrainers[emailKey].firstName,
                        lastName: window.knownTrainers[emailKey].lastName,
                        email: currentUser.email,
                        phone: window.knownTrainers[emailKey].phone || ""
                    };
                } else {
                    trainer = {
                        firstName: currentUser.email.split('@')[0],
                        lastName: "",
                        email: currentUser.email,
                        phone: ""
                    };
                }
                localStorage.setItem('gorilla_trainer_profile', JSON.stringify(trainer));
            }

            const display = document.getElementById('trainerInfoDisplay');
            const inputsArea = document.getElementById('trainerInputsArea');
            if (!display || !inputsArea) return;

            if (trainer) {
                display.innerHTML = `👤 מחובר כ: <strong>${trainer.firstName} ${trainer.lastName}</strong> (${trainer.email}${trainer.phone ? ' | ' + trainer.phone : ''}) <button onclick="editTrainerProfile()" style="background:none; border:none; color:#3498db; cursor:pointer; font-size:0.85em; text-decoration:underline; margin-right:8px;">[שנה פרטים]</button>`;
                inputsArea.style.display = 'none';
            } else {
                display.innerHTML = `👤 התחברות מדריך:`;
                inputsArea.innerHTML = `
                    <input type="text" id="tFirstName" placeholder="שם פרטי">
                    <input type="text" id="tLastName" placeholder="שם משפחה">
                    <input type="email" id="tEmail" placeholder="כתובת מייל">
                    <input type="tel" id="tPhone" placeholder="מספר טלפון">
                    <button class="trainer-save-btn" onclick="saveTrainerProfile()">שמור פרופיל 💾</button>
                `;
                inputsArea.style.display = 'flex';
            }

            checkUserTodoReminders();
        };

        function saveTrainerProfile() {
            const fName = document.getElementById('tFirstName')?.value.trim();
            const lName = document.getElementById('tLastName')?.value.trim();
            const email = document.getElementById('tEmail')?.value.trim();
            const phone = document.getElementById('tPhone')?.value.trim();

            if (!fName || !lName || !email || !phone) {
                alert('אנא מלא שם פרטי, שם משפחה, כתובת מייל ומספר טלפון.');
                return;
            }

            const profile = { firstName: fName, lastName: lName, email: email, phone: phone };
            localStorage.setItem('gorilla_trainer_profile', JSON.stringify(profile));
            window.initTrainerProfile();
            alert('הפרטים נשמרו בהצלחה!');
        }

        function editTrainerProfile() {
            localStorage.removeItem('gorilla_trainer_profile');
            window.initTrainerProfile();
        }

        function exportWeeklyShiftsToCalendar() {
            const trainer = JSON.parse(localStorage.getItem('gorilla_trainer_profile') || 'null');
            if (!trainer) {
                alert('אנא הזן את פרטי המדריך שלך בראש העמוד לפני שליחת המשמרות.');
                window.scrollTo({ top: 0, behavior: 'smooth' });
                return;
            }

            if (monthWeeksCache.length === 0 || !monthWeeksCache[activeWeekIndex]) return;
            const currentWeekObj = monthWeeksCache[activeWeekIndex];
            const nextWeekObj = monthWeeksCache[activeWeekIndex + 1];

            let targetWeekObj = currentWeekObj;
            if (nextWeekObj) {
                let choice = prompt(`בחר איזה שבוע לשלוח לוואטסאפ:\n1) שבוע ${currentWeekObj.weekNum} (הנוכחי)\n2) שבוע ${nextWeekObj.weekNum} (הבא)\n\nהקלד 1 או 2:`, "1");
                if (!choice) return;
                if (choice.trim() === "2") targetWeekObj = nextWeekObj;
            }

            let trainerShifts = [];
            targetWeekObj.days.forEach(dayInfo => {
                const monthData = getMonthDataCache(dayInfo.month);
                const nRows = monthData.north.filter(item => item.dayNum === dayInfo.day);
                const sRows = monthData.south.filter(item => item.dayNum === dayInfo.day);

                [...nRows, ...sRows].forEach(item => {
                    const guide1 = item.values[1] || '';
                    const guide2 = item.values[10] || '';
                    if (trainer.firstName && (guide1.includes(trainer.firstName) || guide2.includes(trainer.firstName))) {
                        trainerShifts.push({ date: dayInfo.day, month: dayInfo.month + 1, unit: item.values[2], loc: item.values[3], sys: item.values[4], hours: item.values[8] });
                    }
                });
            });

            if (trainerShifts.length === 0) {
                alert(`לא נמצאו משמרות הרשומות על שם "${trainer.firstName}" בשבוע ${targetWeekObj.weekNum}.`);
                return;
            }

            let shiftsText = `שלום ${trainer.firstName},\nלהלן פירוט המשמרות שלך לשבוע ${targetWeekObj.weekNum}:\n\n`;
            trainerShifts.forEach(s => {
                shiftsText += `• תאריך: ${s.date}/${s.month} | יחידה: ${s.unit} | מיקום: ${s.loc} | מערכת: ${s.sys} | שעות: ${s.hours || 'לפי תיאום'}\n`;
            });

            let cleanPhone = trainer.phone ? trainer.phone.replace(/\D/g, '') : '';
            let waUrl = `https://wa.me/?text=${encodeURIComponent(shiftsText)}`;
            if (cleanPhone) {
                if (cleanPhone.startsWith('0')) cleanPhone = '972' + cleanPhone.substring(1);
                waUrl = `https://wa.me/${cleanPhone}?text=${encodeURIComponent(shiftsText)}`;
            }

            window.open(waUrl, '_blank');
        }

        function sendTomorrowReminder(side) {
            const tomorrow = new Date();
            tomorrow.setDate(tomorrow.getDate() + 1);
            const mIdx = tomorrow.getMonth();
            const dNum = tomorrow.getDate();
            const monthData = getMonthDataCache(mIdx);
            
            const rows = monthData[side].filter(item => item.dayNum === dNum);
            if (!rows || rows.length === 0) {
                alert("לא נמצאו נתונים למחר.");
                return;
            }

            const activeRows = rows.filter(item => {
                const notes = item.values[9] || '';
                return !notes.includes('בוטל') && !notes.includes('התבטל');
            });

            if (activeRows.length === 0) {
                alert("כל האימונים המיועדים למחר מבוטלים.");
                return;
            }

            const trainer = JSON.parse(localStorage.getItem('gorilla_trainer_profile') || 'null');
            let selectedRows = activeRows;

            if (trainer && trainer.firstName) {
                const matchedRows = activeRows.filter(item => {
                    const guide1 = item.values[1] || '';
                    const guide2 = item.values[10] || '';
                    return guide1.includes(trainer.firstName) || guide2.includes(trainer.firstName);
                });
                if (matchedRows.length > 0) {
                    selectedRows = matchedRows;
                }
            }

            let hoursStr = selectedRows.map(r => r.values[8] || 'לפי תיאום').join(' | ');
            let targetPhone = "";

            selectedRows.forEach(rowObj => {
                const r = rowObj.values;
                if (r[5] && /\d{9,}/.test(r[5])) {
                    targetPhone = r[5];
                }
            });

            let msg = `מה המצב?\nזה מהצוות גיל של בגירה\nמחר אנחנו מגיעים אליך לאימון\nבשעות: ${hoursStr}\nנתראה!`;

            let waUrl = `https://wa.me/?text=${encodeURIComponent(msg)}`;
            if (targetPhone) {
                let cleanPhone = targetPhone.replace(/\D/g, '');
                if (cleanPhone.startsWith('0')) cleanPhone = '972' + cleanPhone.substring(1);
                waUrl = `https://wa.me/${cleanPhone}?text=${encodeURIComponent(msg)}`;
            }

            window.open(waUrl, '_blank');
        }

        function updateRowStatus(selectElement) {
            const row = selectElement.closest('tr');
            const notesInput = row.querySelector('.notes-input');
            if (selectElement.value === 'לא תקין') {
                let faultNotes = prompt("אנא הזן את פירוט התקלה החדשה:");
                if (faultNotes && faultNotes.trim() !== "") {
                    let currentVal = notesInput.value.trim();
                    notesInput.value = currentVal ? currentVal + " | " + faultNotes.trim() : faultNotes.trim();
                }
            }
            saveStatusData();
        }

        function toggleTheme() {
            document.body.classList.toggle('dark-mode');
            const isDark = document.body.classList.contains('dark-mode');
            localStorage.setItem('gorilla_theme', isDark ? 'dark' : 'light');
            const tBtn = document.getElementById('themeToggleBtn');
            if (tBtn) tBtn.innerText = isDark ? '☀️ מצב בהיר' : '🌙 מצב כהה';
            renderDashboard(activeDashboardMonth);
        }

        function switchTab(tabId, event, save = true) {
            document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
            document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
            const targetTab = document.getElementById(tabId);
            if (targetTab) targetTab.classList.add('active');
            
            const btn = document.querySelector(`.tab-btn[onclick*="${tabId}"]`);
            if (btn) btn.classList.add('active');
            else if (event && event.currentTarget) event.currentTarget.classList.add('active');

            if (save) localStorage.setItem('gorilla_active_tab', tabId);
            
            if (tabId === 'dashboard') {
                renderDashboard(activeDashboardMonth);
            }
            
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function filterSchedule() {
            const searchEl = document.getElementById("scheduleSearch");
            if (!searchEl) return;
            
            const rawInput = searchEl.value.trim().toUpperCase();
            const terms = rawInput.split(/\s+/).filter(t => t.length > 0);

            document.querySelectorAll(".spreadsheet-container table tbody tr").forEach(row => {
                if (terms.length === 0) {
                    row.style.display = "";
                    return;
                }

                let contextText = "";
                if (row.closest("#sheetNorthTable")) {
                    contextText = " צפון ניידת 1 ";
                } else if (row.closest("#sheetSouthTable")) {
                    contextText = " דרום מרכז ניידת 2 ";
                }

                let rowValues = [contextText];
                
                row.querySelectorAll("input").forEach(inp => {
                    if (inp.value && inp.value.trim()) {
                        rowValues.push(inp.value.trim());
                    }
                });

                row.querySelectorAll("select").forEach(sel => {
                    if (sel.value && sel.value.trim()) {
                        rowValues.push(sel.value.trim());
                    }
                });

                row.querySelectorAll("td").forEach(td => {
                    Array.from(td.childNodes).forEach(node => {
                        if (node.nodeType === Node.TEXT_NODE && node.textContent.trim()) {
                            rowValues.push(node.textContent.trim());
                        }
                    });
                });

                const textToSearch = rowValues.join(" ").toUpperCase();
                const matchesAll = terms.every(term => textToSearch.includes(term));
                row.style.display = matchesAll ? "" : "none";
            });
        }

        function filterSlides() {
            let input = document.getElementById("slidesSearch").value.toUpperCase();
            document.querySelectorAll("#pdf-slides .slide-box").forEach(box => {
                box.style.display = box.innerText.toUpperCase().includes(input) ? "" : "none";
            });
        }

        function filterFormsTab() {
            let input = document.getElementById("formsSearch").value.toUpperCase();
            document.querySelectorAll("#forms .form-item").forEach(item => {
                item.style.display = item.innerText.toUpperCase().includes(input) ? "" : "none";
            });
        }

        function sendGroupWhatsAppSummary() {
            if (monthWeeksCache.length === 0 || !monthWeeksCache[activeWeekIndex]) return;
            const currentWeekObj = monthWeeksCache[activeWeekIndex];
            let msg = `📋 *סיכום שבועי לקבוצה - שבוע ${currentWeekObj.weekNum}*\n\n`;
            let count = 0;

            currentWeekObj.days.forEach(dayInfo => {
                const monthData = getMonthDataCache(dayInfo.month);
                const dStr = String(dayInfo.day).padStart(2, '0');
                const mStr = String(dayInfo.month + 1).padStart(2, '0');
                let hasDayEntries = false;
                
                ['north', 'south'].forEach(side => {
                    monthData[side].filter(item => item.dayNum === dayInfo.day).forEach(item => {
                        const vals = item.values;
                        if (vals[1] || vals[2]) {
                            let guideStr = vals[1] || 'לא צויין';
                            if (vals[10]) guideStr += ` + ${vals[10]}`;

                            let gorillaStr = vals[7] || 'לא צויין';
                            if (vals[11]) gorillaStr += ` + ${vals[11]}`;

                            let truckStr = vals[12] ? ` | ניידת: ${vals[12]}` : '';

                            msg += `• *יום ${dayInfo.hDayName} (${dStr}.${mStr})* | ${side === 'north' ? 'ניידת 1' : 'ניידת 2'}: ${vals[2]} (${vals[3]}) | מדריך: ${guideStr} | גורילה: ${gorillaStr}${truckStr}\n`;
                            count++;
                            hasDayEntries = true;
                        }
                    });
                });

                if (hasDayEntries) {
                    msg += `\n`;
                }
            });

            if (count === 0) { alert(`לא נמצאו נתונים פעילים בשבוע ${currentWeekObj.weekNum}.`); return; }
            window.open(`https://wa.me/?text=${encodeURIComponent(msg)}`, '_blank');
        }

        function copyText(text, btnElement) {
            if (navigator.clipboard && navigator.clipboard.writeText) {
                navigator.clipboard.writeText(text).then(() => {
                    showCopiedFeedback(btnElement);
                }).catch(() => {
                    fallbackCopyText(text, btnElement);
                });
            } else {
                fallbackCopyText(text, btnElement);
            }
        }

        function fallbackCopyText(text, btnElement) {
            const textArea = document.createElement("textarea");
            textArea.value = text;
            document.body.appendChild(textArea);
            textArea.select();
            try {
                document.execCommand('copy');
                showCopiedFeedback(btnElement);
            } catch (err) {
                alert('שגיאה בהעתקת הקישור');
            }
            document.body.removeChild(textArea);
        }

        function showCopiedFeedback(btnElement) {
            let originalText = btnElement.innerText;
            btnElement.innerText = 'הועתק! ✓';
            setTimeout(() => {
                btnElement.innerText = originalText;
            }, 2000);
        }
    </script>
</body>
</html>
