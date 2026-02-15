You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "ABOUT US | Hi-Tech Imported OLMOS & ITIB Italy machines",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "certificates.html",
    "context": {
      "title": "CERTIFICATES | ARAI | FIELD TESTING STATION | DIMENSION TESTING | QUALITY ASSURANCE LABORATORY | TUV",
      "first_heading": "CERTIFICATES"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "CONTACT US | Sunrise Corrugated (India) Pvt Ltd. | 91 80 27826190, 91 80 27826930",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5e3a198b9f557dce8bcf744d800929a9.css",
    "context": {
      "path": "css/5e3a198b9f557dce8bcf744d800929a9.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/a9e8199f16808a35e5f3e34c5bbd6f10.css",
    "context": {
      "path": "css/a9e8199f16808a35e5f3e34c5bbd6f10.css"
    }
  },
  {
    "path": "css/f401f066ea6611c7fcc32587d80f9123.css",
    "context": {
      "path": "css/f401f066ea6611c7fcc32587d80f9123.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "double-wall-corrugated-hdpe-pipe-dwc.html",
    "context": {
      "title": "DOUBLE WALL CORRUGATED HDPE PIPE (DWC) | Coupler",
      "first_heading": "DOUBLE WALL CORRUGATED HDPE PIPE (DWC)"
    }
  },
  {
    "path": "imgs/1959fd4af099523b3d5806c58272c9f5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/266dd6ef42a256830d88bcae4970a30e.webp",
    "context": {
      "refs": [
        {
          "alt": "In-house Testing Lab",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2874f8c0b657972bc9e568dda85c035f.webp",
    "context": {
      "refs": [
        {
          "alt": "coupler",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/468cacab769e10cc1d39e918174bc3e8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4c682983cb4b4e7b7ad8f2be2061fc87.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/53ab9f14ebc58d95e2e7bf80ae232883.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/54fa0a13b34fd73d1c4b7693d569423b.webp",
    "context": {
      "refs": [
        {
          "alt": "PP Corrugated Flexible Hose Pipe",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55377f2fc83236e9f14ebfd16492ec28.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5a65eb9b91e3c16f0959dd39c04422f5.webp",
    "context": {
      "refs": [
        {
          "alt": "ZEEFLEX Corrugated Flexible Hose Pipes element",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b75a12206e2026af0c6275044600c14.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62f74121596d942ef6e330b0a301d877.webp",
    "context": {
      "refs": [
        {
          "alt": "DIMENSION TESTING",
          "title": ""
        },
        {
          "alt": "Dimension testing",
          "title": ""
        },
        {
          "alt": "Dimension testing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6b50c9bdae44eaaae754f419920b7e96.webp",
    "context": {
      "refs": [
        {
          "alt": "FIELD TESTING STATION",
          "title": ""
        },
        {
          "alt": "FIELD TESTING STATION",
          "title": ""
        },
        {
          "alt": "FIELD TESTING STATION",
          "title": ""
        },
        {
          "alt": "Field testing station",
          "title": ""
        },
        {
          "alt": "Field testing station",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6e06e9d036ffc842c3f914e29082d960.webp",
    "context": {
      "refs": [
        {
          "alt": "PP SINGLE WALL PIPES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6f93aa18a73d34de0d94258c883b5334.webp",
    "context": {
      "refs": [
        {
          "alt": "DOUBLE WALL CORRUGATED HDPE PIPE (DWC) DWC PIPE MANUFACTURERS IN BANGALORE HDPE PIPE MANUFACTURERS I",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70c5a84e0f3d5c77c282a975e4bad726.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7b6ef48d49ec2170561baad9853ecf85.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/845a3f8e3151b14f10aaf44d4f7246c0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/85d723c46dbc3e8b9846c28ac2911b6b.webp",
    "context": {
      "refs": [
        {
          "alt": "Piping Industry",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9d8ecd07a6a714579d4db74822870f35.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0cc85ccc6b05b79b4739ace28cb7156.webp",
    "context": {
      "refs": [
        {
          "alt": "EVA Corrugated Flexible Hose Pipes",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b86602060a1b57836f1cabae7357067b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/be88ca68cabf3d585b221496205ec218.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca348e520350cb5dac5f530c1f8305fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de69f1260ff9e926d6889646e486ff9c.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/e7e9017ece13864ae396256d5685ac04.webp",
    "context": {
      "refs": [
        {
          "alt": "FRPP Corrugated Flexible Hose Pipes",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e7f3ae6934287c232034cbd141425ab6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/effda0fc70361c6f52fee8de7c3db59c.webp",
    "context": {
      "refs": [
        {
          "alt": "QUALITY ASSURANCE LABORATORY",
          "title": ""
        },
        {
          "alt": "Quality assurance laboratory",
          "title": ""
        },
        {
          "alt": "Quality assurance laboratory",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f40ff2d10f3ea3ffaeb834917bf0638c.webp",
    "context": {
      "refs": [
        {
          "alt": "ARAI",
          "title": ""
        },
        {
          "alt": "ARAI",
          "title": ""
        },
        {
          "alt": "ARAI",
          "title": ""
        },
        {
          "alt": "ARAI",
          "title": ""
        },
        {
          "alt": "ARAI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f63e9c541711c084b1a12c05425a1a99.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Home | SUNRISE CORRUGATED | PP SINGLE WALL PIPES DOUBLE WALL | CORRUGATED HDPE PIPE (DWC)",
      "first_heading": "SUNRISE CORRUGATED (INDIA) PVT LTD"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/2b69a948ad8940af2fbaafec3ef111af.js",
    "context": {
      "path": "js/2b69a948ad8940af2fbaafec3ef111af.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/355d290e9e2c44f082719271245c742e.js",
    "context": {
      "path": "js/355d290e9e2c44f082719271245c742e.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "pp-single-wall-pipes.html",
    "context": {
      "title": "PP SINGLE WALL PIPES | Polypropylene corrugated hose pipes",
      "first_heading": "PP SINGLE WALL PIPES"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.