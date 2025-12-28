            border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
            animation: float 6s infinite ease-in-out;
            cursor: pointer;
            pointer-events: auto;
        }

        .balloon:nth-child(odd) {
            background: radial-gradient(circle, #87ceeb, #add8e6);
        }

        .balloon::before {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 20px;
            background: #333;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .popped {
            opacity: 0;
            transform: scale(0);
            transition: all 0.3s;
        }

        footer {
            margin-top: 50px;
            font-size: 1em;
            color: #666;
        }
