# Define a structured schema to represent the conceptual model of Surah 'Abasa
# as a data system based on the interpretation principles (without direct reference to Surah Al-Fatiha texts)

from dataclasses import dataclass, field
from typing import List, Dict

@dataclass
class ConceptNode:
    name: str
    role: str
    function: str
    transitions_to: List[str] = field(default_factory=list)

@dataclass
class SurahModel:
    surah_name: str
    conceptual_nodes: Dict[str, ConceptNode]

# Build the conceptual schema for Surah 'Abasa
abasa_model = SurahModel(
    surah_name="Abasa",
    conceptual_nodes={
        "initial_shock": ConceptNode(
            name="initial_shock",
            role="انفصال إدراكي",
            function="صدمة تعطل نمط التفاعل مع الضعيف",
            transitions_to=["divine_redirection"]
        ),
        "divine_redirection": ConceptNode(
            name="divine_redirection",
            role="إعادة توجيه",
            function="تحويل مركز الوعي إلى معيار القرب الحقيقي",
            transitions_to=["cosmic_weight"]
        ),
        "cosmic_weight": ConceptNode(
            name="cosmic_weight",
            role="تكثيف معرفي",
            function="إبراز الثقل الوجودي للذكر ونتائجه الوجودية",
            transitions_to=["biological_intervention"]
        ),
        "biological_intervention": ConceptNode(
            name="biological_intervention",
            role="فتح حيوي",
            function="استدعاء الجسد كتجلي للعناية والتنظيم",
            transitions_to=["eschatological_unfolding"]
        ),
        "eschatological_unfolding": ConceptNode(
            name="eschatological_unfolding",
            role="انكشاف أخروي",
            function="إظهار هشاشة الإنكار حين يظهر الحد النهائي",
            transitions_to=["existential_evaluation"]
        ),
        "existential_evaluation": ConceptNode(
            name="existential_evaluation",
            role="تقييم وجودي",
            function="حسم موقع الذات حسب استجابتها لمسار القرب والمعرفة",
            transitions_to=[]
        ),
    }
)

abasa_model
